---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625506"
---
# <span data-ttu-id="25bbb-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="25bbb-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="25bbb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="25bbb-103">取得針對金鑰保存庫的憑證通知所註冊的連絡人。</span><span class="sxs-lookup"><span data-stu-id="25bbb-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25bbb-104">句法</span><span class="sxs-lookup"><span data-stu-id="25bbb-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25bbb-105">說明</span><span class="sxs-lookup"><span data-stu-id="25bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="25bbb-106">**AzureKeyVaultCertificateContact** Cmdlet 會取得已針對 Azure 金鑰保存庫中的金鑰電子倉庫的憑證通知登錄的連絡人。</span><span class="sxs-lookup"><span data-stu-id="25bbb-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="25bbb-107">示例</span><span class="sxs-lookup"><span data-stu-id="25bbb-107">EXAMPLES</span></span>

### <span data-ttu-id="25bbb-108">範例1：取得所有憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="25bbb-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="25bbb-109">這個命令會在 Contoso [主要電子倉庫] 中取得證書物件的所有連絡人，然後將它們儲存在 $Contacts 變數中。</span><span class="sxs-lookup"><span data-stu-id="25bbb-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="25bbb-110">參數</span><span class="sxs-lookup"><span data-stu-id="25bbb-110">PARAMETERS</span></span>

### <span data-ttu-id="25bbb-111">-VaultName</span><span class="sxs-lookup"><span data-stu-id="25bbb-111">-VaultName</span></span>
<span data-ttu-id="25bbb-112">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="25bbb-112">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bbb-113">-DefaultProfile</span></span>
<span data-ttu-id="25bbb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25bbb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bbb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bbb-115">CommonParameters</span></span>
<span data-ttu-id="25bbb-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25bbb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bbb-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25bbb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bbb-118">輸入</span><span class="sxs-lookup"><span data-stu-id="25bbb-118">INPUTS</span></span>

## <span data-ttu-id="25bbb-119">輸出</span><span class="sxs-lookup"><span data-stu-id="25bbb-119">OUTPUTS</span></span>

### <span data-ttu-id="25bbb-120">[KeyVault] KeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="25bbb-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="25bbb-121">筆記</span><span class="sxs-lookup"><span data-stu-id="25bbb-121">NOTES</span></span>

## <span data-ttu-id="25bbb-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="25bbb-122">RELATED LINKS</span></span>

[<span data-ttu-id="25bbb-123">附加 AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="25bbb-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="25bbb-124">移除-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="25bbb-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

