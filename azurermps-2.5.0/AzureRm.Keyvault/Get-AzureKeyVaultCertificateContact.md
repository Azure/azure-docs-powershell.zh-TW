---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: d6d2070afcb4a5b9b0b13af1fa54dc93621c5a97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800946"
---
# <span data-ttu-id="c16f6-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c16f6-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="c16f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c16f6-102">SYNOPSIS</span></span>
<span data-ttu-id="c16f6-103">取得針對金鑰保存庫的憑證通知所註冊的連絡人。</span><span class="sxs-lookup"><span data-stu-id="c16f6-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c16f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c16f6-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c16f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c16f6-105">DESCRIPTION</span></span>
<span data-ttu-id="c16f6-106">**AzureKeyVaultCertificateContact** Cmdlet 會取得已針對 Azure 金鑰保存庫中的金鑰電子倉庫的憑證通知登錄的連絡人。</span><span class="sxs-lookup"><span data-stu-id="c16f6-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c16f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="c16f6-107">EXAMPLES</span></span>

### <span data-ttu-id="c16f6-108">範例1：取得所有憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="c16f6-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="c16f6-109">這個命令會在 Contoso [主要電子倉庫] 中取得證書物件的所有連絡人，然後將它們儲存在 $Contacts 變數中。</span><span class="sxs-lookup"><span data-stu-id="c16f6-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="c16f6-110">參數</span><span class="sxs-lookup"><span data-stu-id="c16f6-110">PARAMETERS</span></span>

### <span data-ttu-id="c16f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16f6-111">-DefaultProfile</span></span>
<span data-ttu-id="c16f6-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c16f6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16f6-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c16f6-113">-VaultName</span></span>
<span data-ttu-id="c16f6-114">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c16f6-114">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c16f6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16f6-115">CommonParameters</span></span>
<span data-ttu-id="c16f6-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c16f6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16f6-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c16f6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16f6-118">輸入</span><span class="sxs-lookup"><span data-stu-id="c16f6-118">INPUTS</span></span>

## <span data-ttu-id="c16f6-119">輸出</span><span class="sxs-lookup"><span data-stu-id="c16f6-119">OUTPUTS</span></span>

### <span data-ttu-id="c16f6-120">[KeyVault] KeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="c16f6-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="c16f6-121">筆記</span><span class="sxs-lookup"><span data-stu-id="c16f6-121">NOTES</span></span>

## <span data-ttu-id="c16f6-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="c16f6-122">RELATED LINKS</span></span>

[<span data-ttu-id="c16f6-123">附加 AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c16f6-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="c16f6-124">移除-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c16f6-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

