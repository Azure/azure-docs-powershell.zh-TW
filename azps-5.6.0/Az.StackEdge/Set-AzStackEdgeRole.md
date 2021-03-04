---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 5a6828231b276fc698179d78d3ae4bda7a4c6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901654"
---
# <span data-ttu-id="b24ea-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b24ea-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="b24ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b24ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b24ea-103">更新裝置的角色</span><span class="sxs-lookup"><span data-stu-id="b24ea-103">Updates a Role for a device</span></span>

## <span data-ttu-id="b24ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="b24ea-104">SYNTAX</span></span>

### <span data-ttu-id="b24ea-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b24ea-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b24ea-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24ea-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b24ea-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24ea-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b24ea-108">描述</span><span class="sxs-lookup"><span data-stu-id="b24ea-108">DESCRIPTION</span></span>
<span data-ttu-id="b24ea-109">**Set-AzStackEdgeRole** Cmdlet 會更新 Stack Edge 裝置中的 IoT 角色。</span><span class="sxs-lookup"><span data-stu-id="b24ea-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="b24ea-110">舊安裝共用將會取代為 ShareName 參數中新提供的共用。</span><span class="sxs-lookup"><span data-stu-id="b24ea-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="b24ea-111">例子</span><span class="sxs-lookup"><span data-stu-id="b24ea-111">EXAMPLES</span></span>

### <span data-ttu-id="b24ea-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="b24ea-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="b24ea-113">共用名稱稱會以新提供的共用取代舊安裝共用</span><span class="sxs-lookup"><span data-stu-id="b24ea-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="b24ea-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="b24ea-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="b24ea-115">若要取消卸載所有共用</span><span class="sxs-lookup"><span data-stu-id="b24ea-115">To unmount all shares</span></span>

## <span data-ttu-id="b24ea-116">參數</span><span class="sxs-lookup"><span data-stu-id="b24ea-116">PARAMETERS</span></span>

### <span data-ttu-id="b24ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24ea-117">-DefaultProfile</span></span>
<span data-ttu-id="b24ea-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b24ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24ea-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b24ea-119">-DeviceName</span></span>
<span data-ttu-id="b24ea-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="b24ea-120">Device Name</span></span>

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

### <span data-ttu-id="b24ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b24ea-121">-InputObject</span></span>
<span data-ttu-id="b24ea-122">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="b24ea-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b24ea-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b24ea-123">-Name</span></span>
<span data-ttu-id="b24ea-124">角色名稱</span><span class="sxs-lookup"><span data-stu-id="b24ea-124">Name of the Role</span></span>

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

### <span data-ttu-id="b24ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b24ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="b24ea-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="b24ea-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b24ea-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b24ea-127">-ResourceId</span></span>
<span data-ttu-id="b24ea-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b24ea-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b24ea-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b24ea-129">-ShareName</span></span>
<span data-ttu-id="b24ea-130">在 () 共用您的工作</span><span class="sxs-lookup"><span data-stu-id="b24ea-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="b24ea-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b24ea-131">-Confirm</span></span>
<span data-ttu-id="b24ea-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b24ea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b24ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b24ea-133">-WhatIf</span></span>
<span data-ttu-id="b24ea-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b24ea-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b24ea-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b24ea-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b24ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24ea-136">CommonParameters</span></span>
<span data-ttu-id="b24ea-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b24ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24ea-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b24ea-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24ea-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b24ea-139">INPUTS</span></span>

### <span data-ttu-id="b24ea-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b24ea-140">System.String</span></span>

### <span data-ttu-id="b24ea-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b24ea-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b24ea-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b24ea-142">OUTPUTS</span></span>

### <span data-ttu-id="b24ea-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b24ea-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b24ea-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b24ea-144">NOTES</span></span>

## <span data-ttu-id="b24ea-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b24ea-145">RELATED LINKS</span></span>
