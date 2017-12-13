static void Main(string[] args)
{
string[] characters = "a.b.c.e.f.g.h.i.j.k.l.m.n.o.p.q.r.s.t.u.v.w.x.y.z.0.1.2.3.4.5.6.7.8.9.A.B.C.E.F.G.H.I.J.K.L.M.N.O.P.Q.R.S.T.U.V.W.X.Y.Z. ".Split('.');
         double[] seed = { 48, 2, 14, 13, 20, 57, 32, -1, 8, -2, 7, 7, -1, -13, 3};
         string answer = "";
         for(int i = 0; i < seed.Length; i++)
         {
                  answer = answer + characters[Convert.ToInt32(seed[i] * characters.Length / 63 + i)];
         }
         Console.WriteLine(answer);
}
