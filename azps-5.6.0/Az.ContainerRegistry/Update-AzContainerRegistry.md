---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: aa84186be2b5dc13117397e76722a6826d5314a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903001"
---
# <span data-ttu-id="ade13-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ade13-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="ade13-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ade13-102">SYNOPSIS</span></span>
<span data-ttu-id="ade13-103">更新容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="ade13-103">Updates a container registry.</span></span>

## <span data-ttu-id="ade13-104">語法</span><span class="sxs-lookup"><span data-stu-id="ade13-104">SYNTAX</span></span>

### <span data-ttu-id="ade13-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ade13-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade13-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade13-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade13-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade13-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade13-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade13-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade13-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade13-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade13-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade13-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ade13-111">描述</span><span class="sxs-lookup"><span data-stu-id="ade13-111">DESCRIPTION</span></span>
<span data-ttu-id="ade13-112">Cmdlet Update-AzContainerRegistry更新容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="ade13-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="ade13-113">例子</span><span class="sxs-lookup"><span data-stu-id="ade13-113">EXAMPLES</span></span>

### <span data-ttu-id="ade13-114">範例 1：為指定的容器登錄啟用系統管理員使用者</span><span class="sxs-lookup"><span data-stu-id="ade13-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="ade13-115">此命令可讓系統管理員使用者使用指定的容器登錄。</span><span class="sxs-lookup"><span data-stu-id="ade13-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="ade13-116">範例 2：設定指定容器登錄所使用的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ade13-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="ade13-117">此命令會設定指定的容器登錄，以在同一個訂閱中使用現有的儲存 \` \` 帳戶 mystorageaccount。</span><span class="sxs-lookup"><span data-stu-id="ade13-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="ade13-118">參數</span><span class="sxs-lookup"><span data-stu-id="ade13-118">PARAMETERS</span></span>

### <span data-ttu-id="ade13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade13-119">-DefaultProfile</span></span>
<span data-ttu-id="ade13-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ade13-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ade13-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ade13-121">-DisableAdminUser</span></span>
<span data-ttu-id="ade13-122">啟用容器登錄的系統管理員使用者。</span><span class="sxs-lookup"><span data-stu-id="ade13-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="ade13-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ade13-123">-EnableAdminUser</span></span>
<span data-ttu-id="ade13-124">啟用容器登錄的系統管理員使用者。</span><span class="sxs-lookup"><span data-stu-id="ade13-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="ade13-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ade13-125">-Name</span></span>
<span data-ttu-id="ade13-126">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="ade13-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="ade13-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ade13-127">-NetworkRuleSet</span></span>
<span data-ttu-id="ade13-128">容器註冊表的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="ade13-128">The network rule set for a container registry.</span></span>

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

### <span data-ttu-id="ade13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade13-129">-ResourceGroupName</span></span>
<span data-ttu-id="ade13-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ade13-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ade13-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ade13-131">-ResourceId</span></span>
<span data-ttu-id="ade13-132">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ade13-132">The container registry resource id</span></span>

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

### <span data-ttu-id="ade13-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="ade13-133">-Sku</span></span>
<span data-ttu-id="ade13-134">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="ade13-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="ade13-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ade13-135">-StorageAccountName</span></span>
<span data-ttu-id="ade13-136">現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ade13-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="ade13-137">-標記</span><span class="sxs-lookup"><span data-stu-id="ade13-137">-Tag</span></span>
<span data-ttu-id="ade13-138">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="ade13-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="ade13-139">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ade13-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ade13-140">-確認</span><span class="sxs-lookup"><span data-stu-id="ade13-140">-Confirm</span></span>
<span data-ttu-id="ade13-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ade13-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade13-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade13-142">-WhatIf</span></span>
<span data-ttu-id="ade13-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ade13-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade13-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ade13-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade13-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade13-145">CommonParameters</span></span>
<span data-ttu-id="ade13-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ade13-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade13-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade13-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade13-148">輸入</span><span class="sxs-lookup"><span data-stu-id="ade13-148">INPUTS</span></span>

### <span data-ttu-id="ade13-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ade13-149">System.String</span></span>

## <span data-ttu-id="ade13-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ade13-150">OUTPUTS</span></span>

### <span data-ttu-id="ade13-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ade13-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ade13-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ade13-152">NOTES</span></span>

## <span data-ttu-id="ade13-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ade13-153">RELATED LINKS</span></span>

[<span data-ttu-id="ade13-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ade13-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="ade13-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ade13-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="ade13-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ade13-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

