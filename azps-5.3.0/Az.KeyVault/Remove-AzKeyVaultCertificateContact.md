---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438176"
---
# <span data-ttu-id="4cd8b-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4cd8b-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="4cd8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cd8b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd8b-103">從金鑰保存庫刪除已登錄到證書通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="4cd8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cd8b-104">SYNTAX</span></span>

### <span data-ttu-id="4cd8b-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="4cd8b-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cd8b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="4cd8b-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cd8b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cd8b-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd8b-108">說明</span><span class="sxs-lookup"><span data-stu-id="4cd8b-108">DESCRIPTION</span></span>
<span data-ttu-id="4cd8b-109">**AzKeyVaultCertificateContact** Cmdlet 會從金鑰保存庫中刪除已登錄到證書通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="4cd8b-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cd8b-110">EXAMPLES</span></span>

### <span data-ttu-id="4cd8b-111">範例1：移除憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="4cd8b-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="4cd8b-112">這個命令會以 Contoso01 金鑰電子倉庫的憑證連絡人的身分移除 Patti 更完整的資訊。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="4cd8b-113">如果已指定 PassThru，則 Cmdlet 會傳回剩餘憑證連絡人的清單。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="4cd8b-114">參數</span><span class="sxs-lookup"><span data-stu-id="4cd8b-114">PARAMETERS</span></span>

### <span data-ttu-id="4cd8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd8b-115">-DefaultProfile</span></span>
<span data-ttu-id="4cd8b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4cd8b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cd8b-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="4cd8b-117">-EmailAddress</span></span>
<span data-ttu-id="4cd8b-118">指定要移除之連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="4cd8b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cd8b-119">-InputObject</span></span>
<span data-ttu-id="4cd8b-120">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-120">KeyVault object.</span></span>

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

### <span data-ttu-id="4cd8b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cd8b-121">-PassThru</span></span>
<span data-ttu-id="4cd8b-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4cd8b-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4cd8b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cd8b-124">-ResourceId</span></span>
<span data-ttu-id="4cd8b-125">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="4cd8b-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4cd8b-126">-VaultName</span></span>
<span data-ttu-id="4cd8b-127">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd8b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4cd8b-128">-Confirm</span></span>
<span data-ttu-id="4cd8b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cd8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd8b-130">-WhatIf</span></span>
<span data-ttu-id="4cd8b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd8b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cd8b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd8b-133">CommonParameters</span></span>
<span data-ttu-id="4cd8b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd8b-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd8b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4cd8b-136">INPUTS</span></span>

### <span data-ttu-id="4cd8b-137">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4cd8b-138">System.object</span><span class="sxs-lookup"><span data-stu-id="4cd8b-138">System.String</span></span>

## <span data-ttu-id="4cd8b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4cd8b-139">OUTPUTS</span></span>

### <span data-ttu-id="4cd8b-140">PSKeyVaultCertificateContact 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="4cd8b-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="4cd8b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4cd8b-141">NOTES</span></span>

## <span data-ttu-id="4cd8b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cd8b-142">RELATED LINKS</span></span>

[<span data-ttu-id="4cd8b-143">附加 AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4cd8b-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="4cd8b-144">AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4cd8b-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

