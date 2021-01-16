---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275664"
---
# <span data-ttu-id="d08c4-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d08c4-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="d08c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d08c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d08c4-103">更新容器註冊。</span><span class="sxs-lookup"><span data-stu-id="d08c4-103">Updates a container registry.</span></span>

## <span data-ttu-id="d08c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d08c4-104">SYNTAX</span></span>

### <span data-ttu-id="d08c4-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d08c4-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d08c4-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d08c4-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d08c4-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d08c4-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d08c4-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d08c4-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d08c4-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d08c4-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d08c4-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d08c4-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d08c4-111">說明</span><span class="sxs-lookup"><span data-stu-id="d08c4-111">DESCRIPTION</span></span>
<span data-ttu-id="d08c4-112">Update-AzContainerRegistry Cmdlet 會更新容器註冊。</span><span class="sxs-lookup"><span data-stu-id="d08c4-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="d08c4-113">示例</span><span class="sxs-lookup"><span data-stu-id="d08c4-113">EXAMPLES</span></span>

### <span data-ttu-id="d08c4-114">範例1：針對指定的容器註冊表啟用系統管理員使用者</span><span class="sxs-lookup"><span data-stu-id="d08c4-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="d08c4-115">這個命令可讓系統管理員使用者使用指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="d08c4-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="d08c4-116">範例2：設定指定的樹枝 registry 所使用的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="d08c4-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="d08c4-117">這個命令會將指定的容器登錄設定為 \` \` 在同一個訂閱中使用現有的儲存空間帳戶 mystorageaccount。</span><span class="sxs-lookup"><span data-stu-id="d08c4-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="d08c4-118">參數</span><span class="sxs-lookup"><span data-stu-id="d08c4-118">PARAMETERS</span></span>

### <span data-ttu-id="d08c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08c4-119">-DefaultProfile</span></span>
<span data-ttu-id="d08c4-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d08c4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d08c4-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d08c4-121">-DisableAdminUser</span></span>
<span data-ttu-id="d08c4-122">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="d08c4-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d08c4-123">-EnableAdminUser</span></span>
<span data-ttu-id="d08c4-124">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="d08c4-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d08c4-125">-Name</span></span>
<span data-ttu-id="d08c4-126">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="d08c4-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d08c4-127">-NetworkRuleSet</span></span>
<span data-ttu-id="d08c4-128">容器註冊表的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="d08c4-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d08c4-129">-ResourceGroupName</span></span>
<span data-ttu-id="d08c4-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d08c4-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d08c4-131">-ResourceId</span></span>
<span data-ttu-id="d08c4-132">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d08c4-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="d08c4-133">-Sku</span></span>
<span data-ttu-id="d08c4-134">容器註冊 SKU。</span><span class="sxs-lookup"><span data-stu-id="d08c4-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d08c4-135">-StorageAccountName</span></span>
<span data-ttu-id="d08c4-136">現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d08c4-136">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="d08c4-137">-Tag</span></span>
<span data-ttu-id="d08c4-138">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d08c4-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="d08c4-139">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d08c4-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-140">-確認</span><span class="sxs-lookup"><span data-stu-id="d08c4-140">-Confirm</span></span>
<span data-ttu-id="d08c4-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d08c4-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d08c4-142">-WhatIf</span></span>
<span data-ttu-id="d08c4-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d08c4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d08c4-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d08c4-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08c4-145">CommonParameters</span></span>
<span data-ttu-id="d08c4-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d08c4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08c4-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d08c4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08c4-148">輸入</span><span class="sxs-lookup"><span data-stu-id="d08c4-148">INPUTS</span></span>

### <span data-ttu-id="d08c4-149">System.object</span><span class="sxs-lookup"><span data-stu-id="d08c4-149">System.String</span></span>

## <span data-ttu-id="d08c4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="d08c4-150">OUTPUTS</span></span>

### <span data-ttu-id="d08c4-151">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d08c4-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d08c4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="d08c4-152">NOTES</span></span>

## <span data-ttu-id="d08c4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="d08c4-153">RELATED LINKS</span></span>

[<span data-ttu-id="d08c4-154">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d08c4-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="d08c4-155">AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d08c4-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="d08c4-156">移除-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d08c4-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

