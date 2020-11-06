---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456575"
---
# <span data-ttu-id="fa623-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fa623-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="fa623-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa623-102">SYNOPSIS</span></span>
<span data-ttu-id="fa623-103">建立金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fa623-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa623-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa623-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa623-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa623-105">DESCRIPTION</span></span>
<span data-ttu-id="fa623-106">**新的-AzureRmKeyVault** Cmdlet 會在指定的資源群組中建立金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="fa623-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="fa623-107">這個 Cmdlet 也會授與目前登入的使用者在金鑰保存庫中新增、移除或列出金鑰及密碼的許可權。</span><span class="sxs-lookup"><span data-stu-id="fa623-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="fa623-108">注意：如果您看到錯誤，表示您在嘗試建立新的金鑰保存庫時 **未登錄訂閱使用命名空間 ' KeyVault '** ，請執行 **Register-AzureRmResourceProvider-ProviderNamespace "microsoft. KeyVault"** ，然後重新執行 **新的 AzureRmKeyVault** 命令。</span><span class="sxs-lookup"><span data-stu-id="fa623-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="fa623-109">如需詳細資訊，請參閱註冊 AzureRmResourceProvider。</span><span class="sxs-lookup"><span data-stu-id="fa623-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="fa623-110">示例</span><span class="sxs-lookup"><span data-stu-id="fa623-110">EXAMPLES</span></span>

### <span data-ttu-id="fa623-111">範例1：建立標準的金鑰 vault</span><span class="sxs-lookup"><span data-stu-id="fa623-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="fa623-112">這個命令會在 Azure region （美國）中，建立一個名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fa623-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="fa623-113">該命令會將主要電子倉庫新增到名為 Group14 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="fa623-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="fa623-114">因為命令不會指定 *SKU* 參數的值，所以它會建立標準的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="fa623-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="fa623-115">範例2：建立 Premium 金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="fa623-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="fa623-116">這個命令會建立一個金鑰 vault，就像前一個範例一樣。</span><span class="sxs-lookup"><span data-stu-id="fa623-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="fa623-117">不過，它會為 *SKU* 參數指定 premium 的值，以建立 Premium 金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="fa623-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="fa623-118">參數</span><span class="sxs-lookup"><span data-stu-id="fa623-118">PARAMETERS</span></span>

### <span data-ttu-id="fa623-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="fa623-119">-EnabledForDeployment</span></span>
<span data-ttu-id="fa623-120">當在資源建立期間參照此金鑰保存庫時，可使用 Microsoft. 計算資源提供者來從此金鑰保存庫中取得機密資訊，例如建立虛擬機器時。</span><span class="sxs-lookup"><span data-stu-id="fa623-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fa623-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="fa623-122">讓 Azure 磁片加密服務從此金鑰保存庫取得機密和解除解包金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa623-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="fa623-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="fa623-124">在範本部署中參照此金鑰保存庫時，允許 Azure 資源管理員從該金鑰保存庫取得機密。</span><span class="sxs-lookup"><span data-stu-id="fa623-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="fa623-125">-EnableSoftDelete</span></span>
<span data-ttu-id="fa623-126">如果已指定，則會針對此金鑰保存庫啟用 [虛刪除] 功能。</span><span class="sxs-lookup"><span data-stu-id="fa623-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-127">-位置</span><span class="sxs-lookup"><span data-stu-id="fa623-127">-Location</span></span>
<span data-ttu-id="fa623-128">指定要在其中建立金鑰保存庫的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="fa623-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="fa623-129">使用命令 Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064) 來查看您的選項。</span><span class="sxs-lookup"><span data-stu-id="fa623-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="fa623-130">如需詳細資訊，請輸入 `Get-Help Get-AzureLocation` 。</span><span class="sxs-lookup"><span data-stu-id="fa623-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa623-131">-ResourceGroupName</span></span>
<span data-ttu-id="fa623-132">指定要在其中建立金鑰保存庫的現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa623-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="fa623-133">-Sku</span></span>
<span data-ttu-id="fa623-134">指定主要電子倉庫實例的 SKU。</span><span class="sxs-lookup"><span data-stu-id="fa623-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="fa623-135">如需有關每個 SKU 可用功能的詳細資訊，請參閱 Azure 金鑰 Vault 定價網站 (https://go.microsoft.com/fwlink/?linkid=512521) 。</span><span class="sxs-lookup"><span data-stu-id="fa623-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa623-136">-Tag</span></span>
<span data-ttu-id="fa623-137">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="fa623-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fa623-138">例如：</span><span class="sxs-lookup"><span data-stu-id="fa623-138">For example:</span></span>

<span data-ttu-id="fa623-139">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fa623-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa623-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fa623-140">-VaultName</span></span>
<span data-ttu-id="fa623-141">指定要建立之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa623-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="fa623-142">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="fa623-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="fa623-143">名稱必須以字母或數位開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="fa623-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="fa623-144">名稱必須是通用唯一的。</span><span class="sxs-lookup"><span data-stu-id="fa623-144">The name must be universally unique.</span></span>

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

### <span data-ttu-id="fa623-145">-確認</span><span class="sxs-lookup"><span data-stu-id="fa623-145">-Confirm</span></span>
<span data-ttu-id="fa623-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa623-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa623-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa623-147">-WhatIf</span></span>
<span data-ttu-id="fa623-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa623-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa623-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa623-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa623-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa623-150">-DefaultProfile</span></span>
<span data-ttu-id="fa623-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa623-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa623-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa623-152">CommonParameters</span></span>
<span data-ttu-id="fa623-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa623-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa623-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa623-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa623-155">輸入</span><span class="sxs-lookup"><span data-stu-id="fa623-155">INPUTS</span></span>

## <span data-ttu-id="fa623-156">輸出</span><span class="sxs-lookup"><span data-stu-id="fa623-156">OUTPUTS</span></span>

### <span data-ttu-id="fa623-157">PSVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fa623-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="fa623-158">筆記</span><span class="sxs-lookup"><span data-stu-id="fa623-158">NOTES</span></span>

## <span data-ttu-id="fa623-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa623-159">RELATED LINKS</span></span>

[<span data-ttu-id="fa623-160">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fa623-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="fa623-161">移除-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fa623-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
