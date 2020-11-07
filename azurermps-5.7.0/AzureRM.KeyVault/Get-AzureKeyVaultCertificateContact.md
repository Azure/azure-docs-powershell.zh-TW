---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623816"
---
# <span data-ttu-id="9eb70-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9eb70-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="9eb70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9eb70-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb70-103">取得針對金鑰保存庫的憑證通知所註冊的連絡人。</span><span class="sxs-lookup"><span data-stu-id="9eb70-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eb70-104">句法</span><span class="sxs-lookup"><span data-stu-id="9eb70-104">SYNTAX</span></span>

### <span data-ttu-id="9eb70-105">VaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="9eb70-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9eb70-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9eb70-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9eb70-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9eb70-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9eb70-108">說明</span><span class="sxs-lookup"><span data-stu-id="9eb70-108">DESCRIPTION</span></span>
<span data-ttu-id="9eb70-109">**AzureKeyVaultCertificateContact** Cmdlet 會取得已針對 Azure 金鑰保存庫中的金鑰電子倉庫的憑證通知登錄的連絡人。</span><span class="sxs-lookup"><span data-stu-id="9eb70-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="9eb70-110">示例</span><span class="sxs-lookup"><span data-stu-id="9eb70-110">EXAMPLES</span></span>

### <span data-ttu-id="9eb70-111">範例1：取得所有憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="9eb70-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="9eb70-112">這個命令會在 Contoso [主要電子倉庫] 中取得證書物件的所有連絡人，然後將它們儲存在 $Contacts 變數中。</span><span class="sxs-lookup"><span data-stu-id="9eb70-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="9eb70-113">參數</span><span class="sxs-lookup"><span data-stu-id="9eb70-113">PARAMETERS</span></span>

### <span data-ttu-id="9eb70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb70-114">-DefaultProfile</span></span>
<span data-ttu-id="9eb70-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9eb70-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eb70-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eb70-116">-InputObject</span></span>
<span data-ttu-id="9eb70-117">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="9eb70-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb70-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eb70-118">-ResourceId</span></span>
<span data-ttu-id="9eb70-119">KeyVault Id。</span><span class="sxs-lookup"><span data-stu-id="9eb70-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb70-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9eb70-120">-VaultName</span></span>
<span data-ttu-id="9eb70-121">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb70-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb70-122">CommonParameters</span></span>
<span data-ttu-id="9eb70-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9eb70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb70-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9eb70-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb70-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9eb70-125">INPUTS</span></span>

### <span data-ttu-id="9eb70-126">所有</span><span class="sxs-lookup"><span data-stu-id="9eb70-126">None</span></span>
<span data-ttu-id="9eb70-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9eb70-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9eb70-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9eb70-128">OUTPUTS</span></span>

### <span data-ttu-id="9eb70-129">[KeyVault] PSKeyVaultCertificateContact<清單></span><span class="sxs-lookup"><span data-stu-id="9eb70-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="9eb70-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9eb70-130">NOTES</span></span>

## <span data-ttu-id="9eb70-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eb70-131">RELATED LINKS</span></span>

[<span data-ttu-id="9eb70-132">附加 AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9eb70-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="9eb70-133">移除-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9eb70-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

