---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454896"
---
# <span data-ttu-id="2b55f-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2b55f-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="2b55f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b55f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b55f-103">更新容器註冊。</span><span class="sxs-lookup"><span data-stu-id="2b55f-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b55f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b55f-104">SYNTAX</span></span>

### <span data-ttu-id="2b55f-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="2b55f-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b55f-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b55f-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b55f-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b55f-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b55f-108">說明</span><span class="sxs-lookup"><span data-stu-id="2b55f-108">DESCRIPTION</span></span>
<span data-ttu-id="2b55f-109">**更新-AzureRmContainerRegistry** Cmdlet 會更新容器註冊。</span><span class="sxs-lookup"><span data-stu-id="2b55f-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="2b55f-110">示例</span><span class="sxs-lookup"><span data-stu-id="2b55f-110">EXAMPLES</span></span>

### <span data-ttu-id="2b55f-111">範例1：針對指定的容器註冊表啟用系統管理員使用者</span><span class="sxs-lookup"><span data-stu-id="2b55f-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

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

<span data-ttu-id="2b55f-112">這個命令可讓系統管理員使用者使用指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="2b55f-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="2b55f-113">範例2：設定指定的樹枝 registry 所使用的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="2b55f-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="2b55f-114">這個命令會將指定的容器登錄設定為 `mystorageaccount` 在同一個訂閱中使用現有的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2b55f-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="2b55f-115">參數</span><span class="sxs-lookup"><span data-stu-id="2b55f-115">PARAMETERS</span></span>

### <span data-ttu-id="2b55f-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="2b55f-116">-DisableAdminUser</span></span>
<span data-ttu-id="2b55f-117">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="2b55f-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b55f-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="2b55f-118">-EnableAdminUser</span></span>
<span data-ttu-id="2b55f-119">針對容器登錄啟用 [管理員使用者]。</span><span class="sxs-lookup"><span data-stu-id="2b55f-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b55f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b55f-120">-Name</span></span>
<span data-ttu-id="2b55f-121">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="2b55f-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="2b55f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b55f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b55f-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2b55f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="2b55f-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2b55f-124">-StorageAccountName</span></span>
<span data-ttu-id="2b55f-125">現有儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b55f-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="2b55f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b55f-126">-Tag</span></span>
<span data-ttu-id="2b55f-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2b55f-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b55f-128">例如：</span><span class="sxs-lookup"><span data-stu-id="2b55f-128">For example:</span></span>

<span data-ttu-id="2b55f-129">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2b55f-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b55f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="2b55f-130">-Confirm</span></span>
<span data-ttu-id="2b55f-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b55f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b55f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b55f-132">-WhatIf</span></span>
<span data-ttu-id="2b55f-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b55f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b55f-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b55f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b55f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b55f-135">-DefaultProfile</span></span>
<span data-ttu-id="2b55f-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b55f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b55f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b55f-137">CommonParameters</span></span>
<span data-ttu-id="2b55f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b55f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b55f-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b55f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b55f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="2b55f-140">INPUTS</span></span>

## <span data-ttu-id="2b55f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="2b55f-141">OUTPUTS</span></span>

### <span data-ttu-id="2b55f-142">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2b55f-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="2b55f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="2b55f-143">NOTES</span></span>

## <span data-ttu-id="2b55f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b55f-144">RELATED LINKS</span></span>

[<span data-ttu-id="2b55f-145">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2b55f-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="2b55f-146">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2b55f-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="2b55f-147">移除-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2b55f-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
