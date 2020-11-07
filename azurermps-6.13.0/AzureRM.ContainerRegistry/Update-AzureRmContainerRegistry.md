---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 10321e780532cd522e7cc1d4532baa360350c324
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623557"
---
# <span data-ttu-id="23770-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23770-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="23770-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23770-102">SYNOPSIS</span></span>
<span data-ttu-id="23770-103">更新容器註冊。</span><span class="sxs-lookup"><span data-stu-id="23770-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23770-104">句法</span><span class="sxs-lookup"><span data-stu-id="23770-104">SYNTAX</span></span>

### <span data-ttu-id="23770-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="23770-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23770-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23770-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23770-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23770-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23770-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23770-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23770-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23770-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23770-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23770-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23770-111">說明</span><span class="sxs-lookup"><span data-stu-id="23770-111">DESCRIPTION</span></span>
<span data-ttu-id="23770-112">Update-AzureRmContainerRegistry Cmdlet 會更新容器註冊。</span><span class="sxs-lookup"><span data-stu-id="23770-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="23770-113">示例</span><span class="sxs-lookup"><span data-stu-id="23770-113">EXAMPLES</span></span>

### <span data-ttu-id="23770-114">範例1：針對指定的容器註冊表啟用系統管理員使用者</span><span class="sxs-lookup"><span data-stu-id="23770-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="23770-115">這個命令可讓系統管理員使用者使用指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="23770-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="23770-116">範例2：設定指定的樹枝 registry 所使用的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="23770-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="23770-117">這個命令會將指定的容器登錄設定為 \` \` 在同一個訂閱中使用現有的儲存空間帳戶 mystorageaccount。</span><span class="sxs-lookup"><span data-stu-id="23770-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="23770-118">參數</span><span class="sxs-lookup"><span data-stu-id="23770-118">PARAMETERS</span></span>

### <span data-ttu-id="23770-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23770-119">-DefaultProfile</span></span>
<span data-ttu-id="23770-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="23770-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23770-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="23770-121">-DisableAdminUser</span></span>
<span data-ttu-id="23770-122">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="23770-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="23770-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="23770-123">-EnableAdminUser</span></span>
<span data-ttu-id="23770-124">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="23770-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="23770-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="23770-125">-Name</span></span>
<span data-ttu-id="23770-126">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="23770-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="23770-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23770-127">-ResourceGroupName</span></span>
<span data-ttu-id="23770-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="23770-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="23770-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23770-129">-ResourceId</span></span>
<span data-ttu-id="23770-130">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="23770-130">The container registry resource id</span></span>

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

### <span data-ttu-id="23770-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="23770-131">-Sku</span></span>
<span data-ttu-id="23770-132">容器註冊 SKU。</span><span class="sxs-lookup"><span data-stu-id="23770-132">Container Registry SKU.</span></span>

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

### <span data-ttu-id="23770-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="23770-133">-StorageAccountName</span></span>
<span data-ttu-id="23770-134">現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="23770-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="23770-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="23770-135">-Tag</span></span>
<span data-ttu-id="23770-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="23770-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="23770-137">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="23770-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="23770-138">-確認</span><span class="sxs-lookup"><span data-stu-id="23770-138">-Confirm</span></span>
<span data-ttu-id="23770-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23770-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23770-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23770-140">-WhatIf</span></span>
<span data-ttu-id="23770-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23770-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23770-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23770-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23770-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23770-143">CommonParameters</span></span>
<span data-ttu-id="23770-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23770-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23770-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23770-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23770-146">輸入</span><span class="sxs-lookup"><span data-stu-id="23770-146">INPUTS</span></span>

### <span data-ttu-id="23770-147">System.object</span><span class="sxs-lookup"><span data-stu-id="23770-147">System.String</span></span>

## <span data-ttu-id="23770-148">輸出</span><span class="sxs-lookup"><span data-stu-id="23770-148">OUTPUTS</span></span>

### <span data-ttu-id="23770-149">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23770-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="23770-150">筆記</span><span class="sxs-lookup"><span data-stu-id="23770-150">NOTES</span></span>

## <span data-ttu-id="23770-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="23770-151">RELATED LINKS</span></span>

[<span data-ttu-id="23770-152">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23770-152">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="23770-153">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23770-153">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="23770-154">移除-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23770-154">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)
