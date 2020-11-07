---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625299"
---
# <span data-ttu-id="2dbf8-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2dbf8-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2dbf8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2dbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbf8-103">取得針對金鑰保存庫的憑證通知所註冊的連絡人。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dbf8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2dbf8-104">SYNTAX</span></span>

### <span data-ttu-id="2dbf8-105">VaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="2dbf8-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dbf8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2dbf8-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dbf8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2dbf8-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dbf8-108">說明</span><span class="sxs-lookup"><span data-stu-id="2dbf8-108">DESCRIPTION</span></span>
<span data-ttu-id="2dbf8-109">**AzureKeyVaultCertificateContact** Cmdlet 會取得已針對 Azure 金鑰保存庫中的金鑰電子倉庫的憑證通知登錄的連絡人。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="2dbf8-110">示例</span><span class="sxs-lookup"><span data-stu-id="2dbf8-110">EXAMPLES</span></span>

### <span data-ttu-id="2dbf8-111">範例1：取得所有憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="2dbf8-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="2dbf8-112">這個命令會在 Contoso [主要電子倉庫] 中取得證書物件的所有連絡人，然後將它們儲存在 $Contacts 變數中。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="2dbf8-113">參數</span><span class="sxs-lookup"><span data-stu-id="2dbf8-113">PARAMETERS</span></span>

### <span data-ttu-id="2dbf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbf8-114">-DefaultProfile</span></span>
<span data-ttu-id="2dbf8-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2dbf8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dbf8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dbf8-116">-InputObject</span></span>
<span data-ttu-id="2dbf8-117">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbf8-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dbf8-118">-ResourceId</span></span>
<span data-ttu-id="2dbf8-119">KeyVault Id。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-119">KeyVault Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbf8-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2dbf8-120">-VaultName</span></span>
<span data-ttu-id="2dbf8-121">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dbf8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbf8-122">CommonParameters</span></span>
<span data-ttu-id="2dbf8-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbf8-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbf8-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2dbf8-125">INPUTS</span></span>

### <span data-ttu-id="2dbf8-126">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="2dbf8-127">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2dbf8-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2dbf8-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2dbf8-128">System.String</span></span>

## <span data-ttu-id="2dbf8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2dbf8-129">OUTPUTS</span></span>

### <span data-ttu-id="2dbf8-130">PSKeyVaultCertificateContact 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="2dbf8-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2dbf8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2dbf8-131">NOTES</span></span>

## <span data-ttu-id="2dbf8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dbf8-132">RELATED LINKS</span></span>

[<span data-ttu-id="2dbf8-133">附加 AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2dbf8-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="2dbf8-134">移除-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2dbf8-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

