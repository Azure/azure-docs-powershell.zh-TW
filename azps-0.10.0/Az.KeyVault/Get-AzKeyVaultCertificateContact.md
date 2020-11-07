---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794685"
---
# <span data-ttu-id="4b31a-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4b31a-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="4b31a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b31a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b31a-103">取得針對金鑰保存庫的憑證通知所註冊的連絡人。</span><span class="sxs-lookup"><span data-stu-id="4b31a-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="4b31a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b31a-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b31a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b31a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b31a-106">**AzKeyVaultCertificateContact** Cmdlet 會取得已針對 Azure 金鑰保存庫中的金鑰電子倉庫的憑證通知登錄的連絡人。</span><span class="sxs-lookup"><span data-stu-id="4b31a-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4b31a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4b31a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b31a-108">範例1：取得所有憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="4b31a-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="4b31a-109">這個命令會在 Contoso [主要電子倉庫] 中取得證書物件的所有連絡人，然後將它們儲存在 $Contacts 變數中。</span><span class="sxs-lookup"><span data-stu-id="4b31a-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="4b31a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4b31a-110">PARAMETERS</span></span>

### <span data-ttu-id="4b31a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b31a-111">-DefaultProfile</span></span>
<span data-ttu-id="4b31a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4b31a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b31a-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4b31a-113">-VaultName</span></span>
<span data-ttu-id="4b31a-114">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b31a-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="4b31a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b31a-115">CommonParameters</span></span>
<span data-ttu-id="4b31a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b31a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b31a-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b31a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b31a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="4b31a-118">INPUTS</span></span>

### <span data-ttu-id="4b31a-119">所有</span><span class="sxs-lookup"><span data-stu-id="4b31a-119">None</span></span>
<span data-ttu-id="4b31a-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4b31a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b31a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="4b31a-121">OUTPUTS</span></span>

### <span data-ttu-id="4b31a-122">[KeyVault] KeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="4b31a-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="4b31a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="4b31a-123">NOTES</span></span>

## <span data-ttu-id="4b31a-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b31a-124">RELATED LINKS</span></span>

[<span data-ttu-id="4b31a-125">附加 AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4b31a-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="4b31a-126">移除-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4b31a-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

