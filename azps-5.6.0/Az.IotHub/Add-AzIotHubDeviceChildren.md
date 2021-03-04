---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: e41030f30e3c5651aca3ddf716af99c919e6e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913881"
---
# <span data-ttu-id="c58ab-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="c58ab-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="c58ab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c58ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c58ab-103">將非邊緣裝置新增為子女至邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="c58ab-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="c58ab-104">語法</span><span class="sxs-lookup"><span data-stu-id="c58ab-104">SYNTAX</span></span>

### <span data-ttu-id="c58ab-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c58ab-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c58ab-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c58ab-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c58ab-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c58ab-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c58ab-108">描述</span><span class="sxs-lookup"><span data-stu-id="c58ab-108">DESCRIPTION</span></span>
<span data-ttu-id="c58ab-109">將指定的非邊緣裝置識別碼以逗號分隔清單新增為指定邊緣裝置的孩子。</span><span class="sxs-lookup"><span data-stu-id="c58ab-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="c58ab-110">例子</span><span class="sxs-lookup"><span data-stu-id="c58ab-110">EXAMPLES</span></span>

### <span data-ttu-id="c58ab-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c58ab-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="c58ab-112">將非邊緣裝置新增為子女至邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="c58ab-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="c58ab-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="c58ab-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="c58ab-114">將非邊緣裝置新增為子女至邊緣裝置，不論非邊緣裝置已經是其他邊緣裝置的孩子。</span><span class="sxs-lookup"><span data-stu-id="c58ab-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="c58ab-115">參數</span><span class="sxs-lookup"><span data-stu-id="c58ab-115">PARAMETERS</span></span>

### <span data-ttu-id="c58ab-116">-兒童</span><span class="sxs-lookup"><span data-stu-id="c58ab-116">-Children</span></span>
<span data-ttu-id="c58ab-117">子裝置清單 (逗號分隔) 只包含非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="c58ab-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="c58ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c58ab-118">-DefaultProfile</span></span>
<span data-ttu-id="c58ab-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c58ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c58ab-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c58ab-120">-DeviceId</span></span>
<span data-ttu-id="c58ab-121">邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c58ab-121">Id of edge device.</span></span>

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

### <span data-ttu-id="c58ab-122">-強制</span><span class="sxs-lookup"><span data-stu-id="c58ab-122">-Force</span></span>
<span data-ttu-id="c58ab-123">覆寫非邊緣裝置父裝置。</span><span class="sxs-lookup"><span data-stu-id="c58ab-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="c58ab-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c58ab-124">-InputObject</span></span>
<span data-ttu-id="c58ab-125">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c58ab-125">IotHub object</span></span>

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

### <span data-ttu-id="c58ab-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c58ab-126">-IotHubName</span></span>
<span data-ttu-id="c58ab-127">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="c58ab-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c58ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c58ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="c58ab-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="c58ab-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c58ab-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c58ab-130">-ResourceId</span></span>
<span data-ttu-id="c58ab-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c58ab-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c58ab-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c58ab-132">-Confirm</span></span>
<span data-ttu-id="c58ab-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c58ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c58ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c58ab-134">-WhatIf</span></span>
<span data-ttu-id="c58ab-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c58ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c58ab-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c58ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c58ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58ab-137">CommonParameters</span></span>
<span data-ttu-id="c58ab-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c58ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58ab-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c58ab-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58ab-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c58ab-140">INPUTS</span></span>

### <span data-ttu-id="c58ab-141">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c58ab-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c58ab-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c58ab-142">System.String</span></span>

## <span data-ttu-id="c58ab-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c58ab-143">OUTPUTS</span></span>

### <span data-ttu-id="c58ab-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice以</span><span class="sxs-lookup"><span data-stu-id="c58ab-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="c58ab-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c58ab-145">NOTES</span></span>

## <span data-ttu-id="c58ab-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c58ab-146">RELATED LINKS</span></span>
