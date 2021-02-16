---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134475"
---
# <span data-ttu-id="21c7f-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="21c7f-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="21c7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="21c7f-103">更新裝置的角色</span><span class="sxs-lookup"><span data-stu-id="21c7f-103">Updates a Role for a device</span></span>

## <span data-ttu-id="21c7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="21c7f-104">SYNTAX</span></span>

### <span data-ttu-id="21c7f-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="21c7f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c7f-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c7f-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c7f-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c7f-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c7f-108">說明</span><span class="sxs-lookup"><span data-stu-id="21c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="21c7f-109">**AzStackEdgeRole** Cmdlet 會更新堆疊 Edge 裝置的 IoT 角色。</span><span class="sxs-lookup"><span data-stu-id="21c7f-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="21c7f-110">舊的已掛載共用將會以新提供的 [共用名稱] 參數取代。</span><span class="sxs-lookup"><span data-stu-id="21c7f-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="21c7f-111">示例</span><span class="sxs-lookup"><span data-stu-id="21c7f-111">EXAMPLES</span></span>

### <span data-ttu-id="21c7f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="21c7f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="21c7f-113">共用名稱稱會將舊的已裝載共用取代為新提供的共用</span><span class="sxs-lookup"><span data-stu-id="21c7f-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="21c7f-114">範例2</span><span class="sxs-lookup"><span data-stu-id="21c7f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="21c7f-115">若要卸載所有共用</span><span class="sxs-lookup"><span data-stu-id="21c7f-115">To unmount all shares</span></span>

## <span data-ttu-id="21c7f-116">參數</span><span class="sxs-lookup"><span data-stu-id="21c7f-116">PARAMETERS</span></span>

### <span data-ttu-id="21c7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c7f-117">-DefaultProfile</span></span>
<span data-ttu-id="21c7f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21c7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c7f-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="21c7f-119">-DeviceName</span></span>
<span data-ttu-id="21c7f-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="21c7f-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c7f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21c7f-121">-InputObject</span></span>
<span data-ttu-id="21c7f-122">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="21c7f-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21c7f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="21c7f-123">-Name</span></span>
<span data-ttu-id="21c7f-124">角色名稱</span><span class="sxs-lookup"><span data-stu-id="21c7f-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c7f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c7f-125">-ResourceGroupName</span></span>
<span data-ttu-id="21c7f-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="21c7f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c7f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21c7f-127">-ResourceId</span></span>
<span data-ttu-id="21c7f-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="21c7f-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c7f-129">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="21c7f-129">-ShareName</span></span>
<span data-ttu-id="21c7f-130">在角色中共用 (s) </span><span class="sxs-lookup"><span data-stu-id="21c7f-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c7f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="21c7f-131">-Confirm</span></span>
<span data-ttu-id="21c7f-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21c7f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c7f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c7f-133">-WhatIf</span></span>
<span data-ttu-id="21c7f-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21c7f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21c7f-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21c7f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c7f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c7f-136">CommonParameters</span></span>
<span data-ttu-id="21c7f-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21c7f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c7f-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21c7f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c7f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="21c7f-139">INPUTS</span></span>

### <span data-ttu-id="21c7f-140">System.object</span><span class="sxs-lookup"><span data-stu-id="21c7f-140">System.String</span></span>

### <span data-ttu-id="21c7f-141">PSStackEdgeRole （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="21c7f-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="21c7f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="21c7f-142">OUTPUTS</span></span>

### <span data-ttu-id="21c7f-143">PSStackEdgeRole （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="21c7f-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="21c7f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="21c7f-144">NOTES</span></span>

## <span data-ttu-id="21c7f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="21c7f-145">RELATED LINKS</span></span>
