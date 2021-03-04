---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 7cf5070b6f03c7bc19b8d05991314569616c06ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906602"
---
# <span data-ttu-id="8da76-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8da76-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8da76-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8da76-102">SYNOPSIS</span></span>
<span data-ttu-id="8da76-103">新增憑證通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="8da76-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="8da76-104">語法</span><span class="sxs-lookup"><span data-stu-id="8da76-104">SYNTAX</span></span>

### <span data-ttu-id="8da76-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="8da76-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da76-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8da76-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da76-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8da76-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da76-108">描述</span><span class="sxs-lookup"><span data-stu-id="8da76-108">DESCRIPTION</span></span>
<span data-ttu-id="8da76-109">**Add-AzKeyVaultCertificateContact** Cmdlet 會新增 Azure 金鑰保存庫中憑證通知金鑰保存庫的連絡人。</span><span class="sxs-lookup"><span data-stu-id="8da76-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="8da76-110">連絡人會收到有關事件的更新，例如即將到期的憑證、憑證續約等等。</span><span class="sxs-lookup"><span data-stu-id="8da76-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="8da76-111">這些事件是由憑證策略決定。</span><span class="sxs-lookup"><span data-stu-id="8da76-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="8da76-112">例子</span><span class="sxs-lookup"><span data-stu-id="8da76-112">EXAMPLES</span></span>

### <span data-ttu-id="8da76-113">範例 1：新增金鑰庫憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="8da76-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="8da76-114">此命令會將單一百分點陣圖新增為 ContosoKV01 金鑰庫的憑證連絡人，並返回 "ContosoKV01" 庫的連絡人清單。</span><span class="sxs-lookup"><span data-stu-id="8da76-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="8da76-115">參數</span><span class="sxs-lookup"><span data-stu-id="8da76-115">PARAMETERS</span></span>

### <span data-ttu-id="8da76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da76-116">-DefaultProfile</span></span>
<span data-ttu-id="8da76-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8da76-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8da76-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8da76-118">-EmailAddress</span></span>
<span data-ttu-id="8da76-119">指定連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="8da76-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da76-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8da76-120">-InputObject</span></span>
<span data-ttu-id="8da76-121">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="8da76-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8da76-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8da76-122">-PassThru</span></span>
<span data-ttu-id="8da76-123">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8da76-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8da76-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8da76-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da76-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8da76-125">-ResourceId</span></span>
<span data-ttu-id="8da76-126">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8da76-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="8da76-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8da76-127">-VaultName</span></span>
<span data-ttu-id="8da76-128">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8da76-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da76-129">-確認</span><span class="sxs-lookup"><span data-stu-id="8da76-129">-Confirm</span></span>
<span data-ttu-id="8da76-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8da76-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da76-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da76-131">-WhatIf</span></span>
<span data-ttu-id="8da76-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8da76-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da76-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8da76-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da76-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da76-134">CommonParameters</span></span>
<span data-ttu-id="8da76-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8da76-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da76-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8da76-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da76-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8da76-137">INPUTS</span></span>

### <span data-ttu-id="8da76-138">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8da76-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8da76-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8da76-139">System.String</span></span>

## <span data-ttu-id="8da76-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8da76-140">OUTPUTS</span></span>

### <span data-ttu-id="8da76-141">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8da76-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8da76-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8da76-142">NOTES</span></span>

## <span data-ttu-id="8da76-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8da76-143">RELATED LINKS</span></span>

[<span data-ttu-id="8da76-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8da76-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="8da76-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8da76-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

