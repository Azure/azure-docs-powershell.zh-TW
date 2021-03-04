---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: b712f52dac6a369c92f9cd3525460a1946ed5db5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906746"
---
# <span data-ttu-id="17752-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="17752-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="17752-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17752-102">SYNOPSIS</span></span>
<span data-ttu-id="17752-103">更新裝置的角色</span><span class="sxs-lookup"><span data-stu-id="17752-103">Updates a Role for a device</span></span>

## <span data-ttu-id="17752-104">語法</span><span class="sxs-lookup"><span data-stu-id="17752-104">SYNTAX</span></span>

### <span data-ttu-id="17752-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="17752-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17752-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17752-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17752-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17752-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17752-108">描述</span><span class="sxs-lookup"><span data-stu-id="17752-108">DESCRIPTION</span></span>
<span data-ttu-id="17752-109">**Set-AzDataBoxEdgeRole** Cmdlet 會更新 Data Box Edge 裝置上的 IoT 角色。</span><span class="sxs-lookup"><span data-stu-id="17752-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="17752-110">舊安裝共用將會取代為 ShareName 參數中新提供的共用。</span><span class="sxs-lookup"><span data-stu-id="17752-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="17752-111">例子</span><span class="sxs-lookup"><span data-stu-id="17752-111">EXAMPLES</span></span>

### <span data-ttu-id="17752-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="17752-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="17752-113">共用名稱稱會以新提供的共用取代舊安裝共用</span><span class="sxs-lookup"><span data-stu-id="17752-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="17752-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="17752-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="17752-115">若要取消卸載所有共用</span><span class="sxs-lookup"><span data-stu-id="17752-115">To unmount all shares</span></span>

## <span data-ttu-id="17752-116">參數</span><span class="sxs-lookup"><span data-stu-id="17752-116">PARAMETERS</span></span>

### <span data-ttu-id="17752-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17752-117">-DefaultProfile</span></span>
<span data-ttu-id="17752-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="17752-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17752-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="17752-119">-DeviceName</span></span>
<span data-ttu-id="17752-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="17752-120">Device Name</span></span>

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

### <span data-ttu-id="17752-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17752-121">-InputObject</span></span>
<span data-ttu-id="17752-122">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="17752-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17752-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="17752-123">-Name</span></span>
<span data-ttu-id="17752-124">角色名稱</span><span class="sxs-lookup"><span data-stu-id="17752-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17752-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17752-125">-ResourceGroupName</span></span>
<span data-ttu-id="17752-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="17752-126">Resource Group Name</span></span>

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

### <span data-ttu-id="17752-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17752-127">-ResourceId</span></span>
<span data-ttu-id="17752-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="17752-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="17752-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="17752-129">-ShareName</span></span>
<span data-ttu-id="17752-130">在 () 共用您的工作</span><span class="sxs-lookup"><span data-stu-id="17752-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17752-131">-確認</span><span class="sxs-lookup"><span data-stu-id="17752-131">-Confirm</span></span>
<span data-ttu-id="17752-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="17752-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17752-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17752-133">-WhatIf</span></span>
<span data-ttu-id="17752-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17752-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17752-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17752-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17752-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17752-136">CommonParameters</span></span>
<span data-ttu-id="17752-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17752-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17752-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17752-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17752-139">輸入</span><span class="sxs-lookup"><span data-stu-id="17752-139">INPUTS</span></span>

### <span data-ttu-id="17752-140">System.String</span><span class="sxs-lookup"><span data-stu-id="17752-140">System.String</span></span>

### <span data-ttu-id="17752-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="17752-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="17752-142">輸出</span><span class="sxs-lookup"><span data-stu-id="17752-142">OUTPUTS</span></span>

### <span data-ttu-id="17752-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="17752-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="17752-144">筆記</span><span class="sxs-lookup"><span data-stu-id="17752-144">NOTES</span></span>

## <span data-ttu-id="17752-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="17752-145">RELATED LINKS</span></span>
