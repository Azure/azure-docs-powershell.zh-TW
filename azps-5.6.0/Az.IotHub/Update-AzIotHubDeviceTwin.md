---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 84f1485f84996c1c0e98768914afffd501722ab7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908542"
---
# <span data-ttu-id="b3ac1-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="b3ac1-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="b3ac1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ac1-103">更新裝置更新的標記和想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="b3ac1-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3ac1-104">SYNTAX</span></span>

### <span data-ttu-id="b3ac1-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b3ac1-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ac1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3ac1-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3ac1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b3ac1-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3ac1-108">描述</span><span class="sxs-lookup"><span data-stu-id="b3ac1-108">DESCRIPTION</span></span>
<span data-ttu-id="b3ac1-109">更新或取代裝置更新。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="b3ac1-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="b3ac1-111">例子</span><span class="sxs-lookup"><span data-stu-id="b3ac1-111">EXAMPLES</span></span>

### <span data-ttu-id="b3ac1-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="b3ac1-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="b3ac1-113">會返回更新的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="b3ac1-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="b3ac1-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="b3ac1-115">會以更新的所需屬性來返回裝置物件。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="b3ac1-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="b3ac1-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="b3ac1-117">會使用更新的標記屬性來返回裝置物件。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="b3ac1-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="b3ac1-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="b3ac1-119">會返回取代的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="b3ac1-120">參數</span><span class="sxs-lookup"><span data-stu-id="b3ac1-120">PARAMETERS</span></span>

### <span data-ttu-id="b3ac1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ac1-121">-DefaultProfile</span></span>
<span data-ttu-id="b3ac1-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3ac1-123">-需要</span><span class="sxs-lookup"><span data-stu-id="b3ac1-123">-Desired</span></span>
<span data-ttu-id="b3ac1-124">在裝置上新增或更新所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="b3ac1-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b3ac1-125">-DeviceId</span></span>
<span data-ttu-id="b3ac1-126">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-126">Target Device Id.</span></span>

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

### <span data-ttu-id="b3ac1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3ac1-127">-InputObject</span></span>
<span data-ttu-id="b3ac1-128">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="b3ac1-128">IotHub object</span></span>

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

### <span data-ttu-id="b3ac1-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b3ac1-129">-IotHubName</span></span>
<span data-ttu-id="b3ac1-130">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b3ac1-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b3ac1-131">-部分</span><span class="sxs-lookup"><span data-stu-id="b3ac1-131">-Partial</span></span>
<span data-ttu-id="b3ac1-132">僅允許部分更新裝置更新的標記和想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="b3ac1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ac1-133">-ResourceGroupName</span></span>
<span data-ttu-id="b3ac1-134">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="b3ac1-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b3ac1-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3ac1-135">-ResourceId</span></span>
<span data-ttu-id="b3ac1-136">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b3ac1-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b3ac1-137">-標記</span><span class="sxs-lookup"><span data-stu-id="b3ac1-137">-Tag</span></span>
<span data-ttu-id="b3ac1-138">在裝置上新增或更新標記屬性。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="b3ac1-139">-確認</span><span class="sxs-lookup"><span data-stu-id="b3ac1-139">-Confirm</span></span>
<span data-ttu-id="b3ac1-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ac1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ac1-141">-WhatIf</span></span>
<span data-ttu-id="b3ac1-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ac1-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ac1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ac1-144">CommonParameters</span></span>
<span data-ttu-id="b3ac1-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ac1-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b3ac1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ac1-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b3ac1-147">INPUTS</span></span>

### <span data-ttu-id="b3ac1-148">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b3ac1-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b3ac1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b3ac1-149">System.String</span></span>

## <span data-ttu-id="b3ac1-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b3ac1-150">OUTPUTS</span></span>

### <span data-ttu-id="b3ac1-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b3ac1-151">System.String</span></span>

## <span data-ttu-id="b3ac1-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b3ac1-152">NOTES</span></span>

## <span data-ttu-id="b3ac1-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3ac1-153">RELATED LINKS</span></span>
