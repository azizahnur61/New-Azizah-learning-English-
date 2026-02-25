import streamlit as st
from PIL import Image
import os

# --- KONFIGURASI HALAMAN ---
st.set_page_config(page_title="Azizah English Learning", page_icon="🇬🇧", layout="centered")

# --- 1. FOTO SAMPUL ---
# Pastikan file ini sudah di-upload ke GitHub dengan nama yang sama persis
foto_sampul = "IMG_20260225_161910-01.jpeg"

if os.path.exists(foto_sampul):
    image = Image.open(foto_sampul)
    st.image(image, use_container_width=True)
else:
    # Jika foto tidak ditemukan, tampilkan hiasan warna
    st.info("👋 Welcome to Azizah's English Learning App!")

# --- 2. JUDUL & HEADER ---
st.title("🚀 Mari Belajar Bahasa Inggris!")
st.write("Aplikasi ini dirancang khusus untuk membantu kamu menguasai Bahasa Inggris dengan mudah.")

st.markdown("---")

# --- 3. NAVIGASI SIDEBAR ---
with st.sidebar:
    st.header("Main Menu")
    pilihan = st.radio(
        "Pilih materi yang ingin dipelajari:",
        ["Beranda", "Kosakata (Vocabulary)", "Tata Bahasa (Grammar)", "Percakapan (Conversation)", "Tentang Saya"]
    )

# --- 4. ISI MATERI ---

# -- Beranda --
if pilihan == "Beranda":
    st.subheader("Halo, Selamat Datang!")
    st.write("Pilih menu di samping kiri untuk mulai belajar. Jangan lupa untuk mempraktikkan apa yang kamu pelajari hari ini!")
    st.balloons()

# -- Kosakata (Vocabulary) --
elif pilihan == "Kosakata (Vocabulary)":
    st.subheader("📚 Kosakata Harian (Daily Vocabulary)")
    
    tab1, tab2 = st.tabs(["Benda di Rumah", "Kata Kerja"])
    
    with tab1:
        st.write("1. **Window** = Jendela")
        st.write("2. **Door** = Pintu")
        st.write("3. **Kitchen** = Dapur")
        st.write("4. **Bed** = Tempat Tidur")
        
    with tab2:
        st.write("1. **Study** = Belajar")
        st.write("2. **Write** = Menulis")
        st.write("3. **Speak** = Berbicara")
        st.write("4. **Listen** = Mendengar")

# -- Tata Bahasa (Grammar) --
elif pilihan == "Tata Bahasa (Grammar)":
    st.subheader("✍️ Belajar Dasar Grammar")
    st.write("### Simple Present Tense")
    st.write("Digunakan untuk menyatakan fakta atau kebiasaan.")
    st.code("Rumus: I/You/They/We + Verb 1")
    st.write("**Contoh:** I drink milk every morning.")
    
    st.divider()
    
    st.write("### Pronouns (Kata Ganti)")
    st.table({
        "Subject": ["I", "You", "He", "She", "It", "We", "They"],
        "Arti": ["Saya", "Kamu", "Dia (L)", "Dia (P)", "Benda/Hewan", "Kami", "Mereka"]
    })

# -- Percakapan (Conversation) --
elif pilihan == "Percakapan (Conversation)":
    st.subheader("💬 Contoh Percakapan Singkat")
    st.chat_message("user").write("**A:** Hello, how are you today?")
    st.chat_message("assistant").write("**B:** I am fine, thank you. And you?")
    st.chat_message("user").write("**A:** I am great! What are you doing?")
    st.chat_message("assistant").write("**B:** I am learning English with Azizah's App.")

# -- Tentang Saya --
elif pilihan == "Tentang Saya":
    st.subheader("👤 Meet the Author")
    st.write("Halo! Saya **Azizah**.")
    st.write("Saya membuat aplikasi ini untuk membantu teman-teman belajar Bahasa Inggris dengan lebih interaktif.")
    
    st.success("Ingin tanya-tanya? Klik tombol di bawah!")
    st.link_button("Hubungi Saya di WhatsApp", "https://wa.me/628XXXXXXXXXX") # Ganti X dengan nomormu

# --- 5. FOOTER ---
st.markdown("---")
st.caption("© 2026 Azizah English Learning App | Semangat Belajar! 💪")
