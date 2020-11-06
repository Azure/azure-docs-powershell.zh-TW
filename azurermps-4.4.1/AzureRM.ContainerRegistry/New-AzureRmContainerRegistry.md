---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447134"
---
# <span data-ttu-id="7c7eb-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c7eb-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="7c7eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7eb-103">建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c7eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c7eb-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c7eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c7eb-105">DESCRIPTION</span></span>
<span data-ttu-id="7c7eb-106">**新的-AzureRmContainerRegistry** Cmdlet 會建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="7c7eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c7eb-107">EXAMPLES</span></span>

### <span data-ttu-id="7c7eb-108">範例1：使用新的儲存空間帳戶建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="7c7eb-109">這個命令會在 [資源] 群組中使用新的儲存空間帳戶來建立容器註冊表 `MyResourceGroup` 。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="7c7eb-110">範例2：在已啟用系統管理員使用者的情況中建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="7c7eb-111">這個命令會在啟用系統管理員使用者的情況下建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="7c7eb-112">範例3：使用現有的儲存空間帳戶建立容器註冊。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : mystorageaccount
```

<span data-ttu-id="7c7eb-113">這個命令會 `mystorageaccount` 在同一個訂閱中使用現有的儲存空間帳戶來建立容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="7c7eb-114">參數</span><span class="sxs-lookup"><span data-stu-id="7c7eb-114">PARAMETERS</span></span>

### <span data-ttu-id="7c7eb-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="7c7eb-115">-EnableAdminUser</span></span>
<span data-ttu-id="7c7eb-116">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7eb-117">-位置</span><span class="sxs-lookup"><span data-stu-id="7c7eb-117">-Location</span></span>
<span data-ttu-id="7c7eb-118">容器登錄位置。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-118">Container Registry Location.</span></span>
<span data-ttu-id="7c7eb-119">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="7c7eb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c7eb-120">-Name</span></span>
<span data-ttu-id="7c7eb-121">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c7eb-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7eb-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="7c7eb-124">-Sku</span></span>
<span data-ttu-id="7c7eb-125">容器註冊 SKU。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-125">Container Registry SKU.</span></span>
<span data-ttu-id="7c7eb-126">允許的值：基本。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7eb-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c7eb-127">-StorageAccountName</span></span>
<span data-ttu-id="7c7eb-128">現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="7c7eb-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c7eb-129">-Tag</span></span>
<span data-ttu-id="7c7eb-130">以雜湊資料表形式顯示的索引鍵值對。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7c7eb-131">例如：</span><span class="sxs-lookup"><span data-stu-id="7c7eb-131">For example:</span></span>

<span data-ttu-id="7c7eb-132">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7c7eb-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7c7eb-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7c7eb-133">-Confirm</span></span>
<span data-ttu-id="7c7eb-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c7eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c7eb-135">-WhatIf</span></span>
<span data-ttu-id="7c7eb-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c7eb-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c7eb-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7eb-138">-DefaultProfile</span></span>
<span data-ttu-id="7c7eb-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c7eb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7eb-140">CommonParameters</span></span>
<span data-ttu-id="7c7eb-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7eb-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c7eb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7eb-143">輸入</span><span class="sxs-lookup"><span data-stu-id="7c7eb-143">INPUTS</span></span>

## <span data-ttu-id="7c7eb-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7c7eb-144">OUTPUTS</span></span>

### <span data-ttu-id="7c7eb-145">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c7eb-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="7c7eb-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7c7eb-146">NOTES</span></span>

## <span data-ttu-id="7c7eb-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c7eb-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c7eb-148">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c7eb-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="7c7eb-149">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c7eb-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="7c7eb-150">移除-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c7eb-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)