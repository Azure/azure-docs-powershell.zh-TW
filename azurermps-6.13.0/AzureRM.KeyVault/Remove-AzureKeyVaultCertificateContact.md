---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: aee18adf3530976af4b17ffa15f94624248a7db7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449114"
---
# <span data-ttu-id="ca72d-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ca72d-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ca72d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca72d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca72d-103">從金鑰保存庫刪除已登錄到證書通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="ca72d-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca72d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca72d-104">SYNTAX</span></span>

### <span data-ttu-id="ca72d-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="ca72d-105">ByName (Default)</span></span>
```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca72d-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ca72d-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca72d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ca72d-107">ByResourceId</span></span>
```
Remove-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca72d-108">說明</span><span class="sxs-lookup"><span data-stu-id="ca72d-108">DESCRIPTION</span></span>
<span data-ttu-id="ca72d-109">**AzureKeyVaultCertificateContact** Cmdlet 會從金鑰保存庫中刪除已登錄到證書通知的連絡人。</span><span class="sxs-lookup"><span data-stu-id="ca72d-109">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="ca72d-110">示例</span><span class="sxs-lookup"><span data-stu-id="ca72d-110">EXAMPLES</span></span>

### <span data-ttu-id="ca72d-111">範例1：移除憑證連絡人</span><span class="sxs-lookup"><span data-stu-id="ca72d-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="ca72d-112">這個命令會以 Contoso01 金鑰電子倉庫的憑證連絡人的身分移除 Patti 更完整的資訊。</span><span class="sxs-lookup"><span data-stu-id="ca72d-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="ca72d-113">如果已指定 PassThru，則 Cmdlet 會傳回剩餘憑證連絡人的清單。</span><span class="sxs-lookup"><span data-stu-id="ca72d-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="ca72d-114">參數</span><span class="sxs-lookup"><span data-stu-id="ca72d-114">PARAMETERS</span></span>

### <span data-ttu-id="ca72d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca72d-115">-DefaultProfile</span></span>
<span data-ttu-id="ca72d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ca72d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca72d-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca72d-117">-EmailAddress</span></span>
<span data-ttu-id="ca72d-118">指定要移除之連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="ca72d-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="ca72d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca72d-119">-InputObject</span></span>
<span data-ttu-id="ca72d-120">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="ca72d-120">KeyVault object.</span></span>

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

### <span data-ttu-id="ca72d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca72d-121">-PassThru</span></span>
<span data-ttu-id="ca72d-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ca72d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca72d-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ca72d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca72d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca72d-124">-ResourceId</span></span>
<span data-ttu-id="ca72d-125">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca72d-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="ca72d-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ca72d-126">-VaultName</span></span>
<span data-ttu-id="ca72d-127">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca72d-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ca72d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ca72d-128">-Confirm</span></span>
<span data-ttu-id="ca72d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca72d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca72d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca72d-130">-WhatIf</span></span>
<span data-ttu-id="ca72d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca72d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca72d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca72d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca72d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca72d-133">CommonParameters</span></span>
<span data-ttu-id="ca72d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca72d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca72d-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca72d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca72d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ca72d-136">INPUTS</span></span>

### <span data-ttu-id="ca72d-137">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ca72d-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="ca72d-138">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ca72d-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ca72d-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ca72d-139">System.String</span></span>

## <span data-ttu-id="ca72d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ca72d-140">OUTPUTS</span></span>

### <span data-ttu-id="ca72d-141">PSKeyVaultCertificateContact 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ca72d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ca72d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ca72d-142">NOTES</span></span>

## <span data-ttu-id="ca72d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca72d-143">RELATED LINKS</span></span>

[<span data-ttu-id="ca72d-144">附加 AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ca72d-144">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="ca72d-145">AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ca72d-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

