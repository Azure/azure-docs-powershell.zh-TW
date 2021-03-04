---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 4a8eb9ce6fce4cf9719e365055cab5743d081b1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915465"
---
# <span data-ttu-id="59a5e-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59a5e-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="59a5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="59a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="59a5e-103">獲得已註冊金鑰庫憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="59a5e-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="59a5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="59a5e-104">SYNTAX</span></span>

### <span data-ttu-id="59a5e-105">VaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="59a5e-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59a5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="59a5e-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59a5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59a5e-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59a5e-108">描述</span><span class="sxs-lookup"><span data-stu-id="59a5e-108">DESCRIPTION</span></span>
<span data-ttu-id="59a5e-109">**Get-AzKeyVaultCertificateContact** Cmdlet 會取得已註冊 Azure 金鑰保存庫金鑰保存庫憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="59a5e-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="59a5e-110">例子</span><span class="sxs-lookup"><span data-stu-id="59a5e-110">EXAMPLES</span></span>

### <span data-ttu-id="59a5e-111">範例 1：取得所有憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="59a5e-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="59a5e-112">此命令會獲得 Contoso 金鑰保存庫中憑證物件的所有連絡人，然後將這些連絡人儲存在$Contacts變數中。</span><span class="sxs-lookup"><span data-stu-id="59a5e-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="59a5e-113">參數</span><span class="sxs-lookup"><span data-stu-id="59a5e-113">PARAMETERS</span></span>

### <span data-ttu-id="59a5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a5e-114">-DefaultProfile</span></span>
<span data-ttu-id="59a5e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="59a5e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a5e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59a5e-116">-InputObject</span></span>
<span data-ttu-id="59a5e-117">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="59a5e-117">KeyVault object.</span></span>

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

### <span data-ttu-id="59a5e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59a5e-118">-ResourceId</span></span>
<span data-ttu-id="59a5e-119">KeyVault Id。</span><span class="sxs-lookup"><span data-stu-id="59a5e-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="59a5e-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="59a5e-120">-VaultName</span></span>
<span data-ttu-id="59a5e-121">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="59a5e-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="59a5e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a5e-122">CommonParameters</span></span>
<span data-ttu-id="59a5e-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="59a5e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a5e-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59a5e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a5e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="59a5e-125">INPUTS</span></span>

### <span data-ttu-id="59a5e-126">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="59a5e-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="59a5e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="59a5e-127">System.String</span></span>

## <span data-ttu-id="59a5e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="59a5e-128">OUTPUTS</span></span>

### <span data-ttu-id="59a5e-129">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59a5e-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="59a5e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="59a5e-130">NOTES</span></span>

## <span data-ttu-id="59a5e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="59a5e-131">RELATED LINKS</span></span>

[<span data-ttu-id="59a5e-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59a5e-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="59a5e-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59a5e-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

