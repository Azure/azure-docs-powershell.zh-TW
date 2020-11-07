---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958017"
---
# <span data-ttu-id="168b6-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="168b6-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="168b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="168b6-102">SYNOPSIS</span></span>
<span data-ttu-id="168b6-103">更新 IoT 裝置模組雙子的標記和所需屬性。</span><span class="sxs-lookup"><span data-stu-id="168b6-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="168b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="168b6-104">SYNTAX</span></span>

### <span data-ttu-id="168b6-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="168b6-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="168b6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="168b6-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="168b6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="168b6-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="168b6-108">說明</span><span class="sxs-lookup"><span data-stu-id="168b6-108">DESCRIPTION</span></span>
<span data-ttu-id="168b6-109">更新或取代 device 雙子。</span><span class="sxs-lookup"><span data-stu-id="168b6-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="168b6-110">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins 。</span><span class="sxs-lookup"><span data-stu-id="168b6-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="168b6-111">示例</span><span class="sxs-lookup"><span data-stu-id="168b6-111">EXAMPLES</span></span>

### <span data-ttu-id="168b6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="168b6-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="168b6-113">傳回更新的 device module 雙子物件。</span><span class="sxs-lookup"><span data-stu-id="168b6-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="168b6-114">範例2</span><span class="sxs-lookup"><span data-stu-id="168b6-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="168b6-115">傳回具有更新之所需屬性的裝置模組雙子出物件。</span><span class="sxs-lookup"><span data-stu-id="168b6-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="168b6-116">範例3</span><span class="sxs-lookup"><span data-stu-id="168b6-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="168b6-117">傳回含 [更新的標籤] 屬性的裝置模組 [成雙子] 物件。</span><span class="sxs-lookup"><span data-stu-id="168b6-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="168b6-118">範例4</span><span class="sxs-lookup"><span data-stu-id="168b6-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="168b6-119">傳回取代的裝置模組雙子物件。</span><span class="sxs-lookup"><span data-stu-id="168b6-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="168b6-120">參數</span><span class="sxs-lookup"><span data-stu-id="168b6-120">PARAMETERS</span></span>

### <span data-ttu-id="168b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168b6-121">-DefaultProfile</span></span>
<span data-ttu-id="168b6-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="168b6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="168b6-123">-所需</span><span class="sxs-lookup"><span data-stu-id="168b6-123">-Desired</span></span>
<span data-ttu-id="168b6-124">新增或更新模組雙子中所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="168b6-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="168b6-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="168b6-125">-DeviceId</span></span>
<span data-ttu-id="168b6-126">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="168b6-126">Target Device Id.</span></span>

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

### <span data-ttu-id="168b6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="168b6-127">-InputObject</span></span>
<span data-ttu-id="168b6-128">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="168b6-128">IotHub object</span></span>

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

### <span data-ttu-id="168b6-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="168b6-129">-IotHubName</span></span>
<span data-ttu-id="168b6-130">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="168b6-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="168b6-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="168b6-131">-ModuleId</span></span>
<span data-ttu-id="168b6-132">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="168b6-132">Target Module Id.</span></span>

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

### <span data-ttu-id="168b6-133">-部分</span><span class="sxs-lookup"><span data-stu-id="168b6-133">-Partial</span></span>
<span data-ttu-id="168b6-134">僅允許部分更新模組雙子格的標記和所需屬性。</span><span class="sxs-lookup"><span data-stu-id="168b6-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="168b6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="168b6-135">-ResourceGroupName</span></span>
<span data-ttu-id="168b6-136">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="168b6-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="168b6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="168b6-137">-ResourceId</span></span>
<span data-ttu-id="168b6-138">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="168b6-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="168b6-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="168b6-139">-Tag</span></span>
<span data-ttu-id="168b6-140">新增或更新模組雙子中的 tags 屬性。</span><span class="sxs-lookup"><span data-stu-id="168b6-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="168b6-141">-確認</span><span class="sxs-lookup"><span data-stu-id="168b6-141">-Confirm</span></span>
<span data-ttu-id="168b6-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="168b6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="168b6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="168b6-143">-WhatIf</span></span>
<span data-ttu-id="168b6-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="168b6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="168b6-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="168b6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="168b6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168b6-146">CommonParameters</span></span>
<span data-ttu-id="168b6-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="168b6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168b6-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="168b6-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168b6-149">輸入</span><span class="sxs-lookup"><span data-stu-id="168b6-149">INPUTS</span></span>

### <span data-ttu-id="168b6-150">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="168b6-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="168b6-151">System.object</span><span class="sxs-lookup"><span data-stu-id="168b6-151">System.String</span></span>

## <span data-ttu-id="168b6-152">輸出</span><span class="sxs-lookup"><span data-stu-id="168b6-152">OUTPUTS</span></span>

### <span data-ttu-id="168b6-153">PSModuleTwin （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="168b6-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="168b6-154">筆記</span><span class="sxs-lookup"><span data-stu-id="168b6-154">NOTES</span></span>

## <span data-ttu-id="168b6-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="168b6-155">RELATED LINKS</span></span>
