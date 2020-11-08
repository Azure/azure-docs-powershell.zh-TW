---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139227"
---
# <span data-ttu-id="40816-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="40816-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="40816-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40816-102">SYNOPSIS</span></span>
<span data-ttu-id="40816-103">將非邊緣裝置新增為邊緣裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="40816-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="40816-104">句法</span><span class="sxs-lookup"><span data-stu-id="40816-104">SYNTAX</span></span>

### <span data-ttu-id="40816-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="40816-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40816-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40816-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40816-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="40816-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40816-108">說明</span><span class="sxs-lookup"><span data-stu-id="40816-108">DESCRIPTION</span></span>
<span data-ttu-id="40816-109">將非 edge 裝置識別碼的指定逗號分隔清單加上指定的 edge 裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="40816-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="40816-110">示例</span><span class="sxs-lookup"><span data-stu-id="40816-110">EXAMPLES</span></span>

### <span data-ttu-id="40816-111">範例1</span><span class="sxs-lookup"><span data-stu-id="40816-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="40816-112">將非邊緣裝置新增為邊緣裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="40816-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="40816-113">範例2</span><span class="sxs-lookup"><span data-stu-id="40816-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="40816-114">將非邊緣裝置新增為邊緣裝置的子系 irrespectively 非邊緣裝置已是其他 edge 裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="40816-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="40816-115">參數</span><span class="sxs-lookup"><span data-stu-id="40816-115">PARAMETERS</span></span>

### <span data-ttu-id="40816-116">-兒童</span><span class="sxs-lookup"><span data-stu-id="40816-116">-Children</span></span>
<span data-ttu-id="40816-117">子裝置清單 (逗號分隔) 只包含非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="40816-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40816-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40816-118">-DefaultProfile</span></span>
<span data-ttu-id="40816-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40816-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40816-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="40816-120">-DeviceId</span></span>
<span data-ttu-id="40816-121">Edge 裝置的 Id。</span><span class="sxs-lookup"><span data-stu-id="40816-121">Id of edge device.</span></span>

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

### <span data-ttu-id="40816-122">-Force</span><span class="sxs-lookup"><span data-stu-id="40816-122">-Force</span></span>
<span data-ttu-id="40816-123">覆寫非邊緣裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="40816-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="40816-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40816-124">-InputObject</span></span>
<span data-ttu-id="40816-125">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="40816-125">IotHub object</span></span>

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

### <span data-ttu-id="40816-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="40816-126">-IotHubName</span></span>
<span data-ttu-id="40816-127">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="40816-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="40816-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40816-128">-ResourceGroupName</span></span>
<span data-ttu-id="40816-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="40816-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="40816-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40816-130">-ResourceId</span></span>
<span data-ttu-id="40816-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="40816-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="40816-132">-確認</span><span class="sxs-lookup"><span data-stu-id="40816-132">-Confirm</span></span>
<span data-ttu-id="40816-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40816-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40816-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40816-134">-WhatIf</span></span>
<span data-ttu-id="40816-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40816-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40816-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40816-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40816-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40816-137">CommonParameters</span></span>
<span data-ttu-id="40816-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40816-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40816-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40816-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40816-140">輸入</span><span class="sxs-lookup"><span data-stu-id="40816-140">INPUTS</span></span>

### <span data-ttu-id="40816-141">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="40816-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="40816-142">System.object</span><span class="sxs-lookup"><span data-stu-id="40816-142">System.String</span></span>

## <span data-ttu-id="40816-143">輸出</span><span class="sxs-lookup"><span data-stu-id="40816-143">OUTPUTS</span></span>

### <span data-ttu-id="40816-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="40816-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="40816-145">筆記</span><span class="sxs-lookup"><span data-stu-id="40816-145">NOTES</span></span>

## <span data-ttu-id="40816-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="40816-146">RELATED LINKS</span></span>