---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: 72e9b809ac2b2894b34aefeddd17473cc29d9f35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909701"
---
# <span data-ttu-id="6446c-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="6446c-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="6446c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6446c-102">SYNOPSIS</span></span>
<span data-ttu-id="6446c-103">更新 IoT 裝置模組的標記和想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="6446c-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="6446c-104">語法</span><span class="sxs-lookup"><span data-stu-id="6446c-104">SYNTAX</span></span>

### <span data-ttu-id="6446c-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6446c-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6446c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6446c-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6446c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6446c-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6446c-108">描述</span><span class="sxs-lookup"><span data-stu-id="6446c-108">DESCRIPTION</span></span>
<span data-ttu-id="6446c-109">更新或取代裝置更新。</span><span class="sxs-lookup"><span data-stu-id="6446c-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="6446c-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6446c-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="6446c-111">例子</span><span class="sxs-lookup"><span data-stu-id="6446c-111">EXAMPLES</span></span>

### <span data-ttu-id="6446c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="6446c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="6446c-113">會返回更新的裝置模組物件。</span><span class="sxs-lookup"><span data-stu-id="6446c-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="6446c-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="6446c-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="6446c-115">會以更新的所需屬性，返回裝置模組物件。</span><span class="sxs-lookup"><span data-stu-id="6446c-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="6446c-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="6446c-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="6446c-117">會使用更新的標記屬性，會返回裝置模組物件。</span><span class="sxs-lookup"><span data-stu-id="6446c-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="6446c-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="6446c-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="6446c-119">會返回已取代的裝置模組物件。</span><span class="sxs-lookup"><span data-stu-id="6446c-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="6446c-120">參數</span><span class="sxs-lookup"><span data-stu-id="6446c-120">PARAMETERS</span></span>

### <span data-ttu-id="6446c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6446c-121">-DefaultProfile</span></span>
<span data-ttu-id="6446c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6446c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6446c-123">-需要</span><span class="sxs-lookup"><span data-stu-id="6446c-123">-Desired</span></span>
<span data-ttu-id="6446c-124">新增或更新模組元件中所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="6446c-124">Add or update the desired property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6446c-125">-DeviceId</span></span>
<span data-ttu-id="6446c-126">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6446c-126">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6446c-127">-InputObject</span></span>
<span data-ttu-id="6446c-128">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="6446c-128">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6446c-129">-IotHubName</span></span>
<span data-ttu-id="6446c-130">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="6446c-130">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="6446c-131">-ModuleId</span></span>
<span data-ttu-id="6446c-132">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="6446c-132">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-133">-部分</span><span class="sxs-lookup"><span data-stu-id="6446c-133">-Partial</span></span>
<span data-ttu-id="6446c-134">只允許部分更新模組介面的標記和想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="6446c-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="6446c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6446c-135">-ResourceGroupName</span></span>
<span data-ttu-id="6446c-136">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="6446c-136">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6446c-137">-ResourceId</span></span>
<span data-ttu-id="6446c-138">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6446c-138">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-139">-標記</span><span class="sxs-lookup"><span data-stu-id="6446c-139">-Tag</span></span>
<span data-ttu-id="6446c-140">新增或更新模組介面中的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="6446c-140">Add or update the tags property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-141">-確認</span><span class="sxs-lookup"><span data-stu-id="6446c-141">-Confirm</span></span>
<span data-ttu-id="6446c-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6446c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6446c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6446c-143">-WhatIf</span></span>
<span data-ttu-id="6446c-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6446c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6446c-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6446c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6446c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6446c-146">CommonParameters</span></span>
<span data-ttu-id="6446c-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6446c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6446c-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6446c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6446c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="6446c-149">INPUTS</span></span>

### <span data-ttu-id="6446c-150">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6446c-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6446c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6446c-151">System.String</span></span>

## <span data-ttu-id="6446c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="6446c-152">OUTPUTS</span></span>

### <span data-ttu-id="6446c-153">Microsoft.Azure.Commands.management.IotHub.models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="6446c-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="6446c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="6446c-154">NOTES</span></span>

## <span data-ttu-id="6446c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="6446c-155">RELATED LINKS</span></span>
