---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: 63d364ac12d47f5bb15e877e5076550a0cbd3f16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915773"
---
# <span data-ttu-id="311ec-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="311ec-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="311ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="311ec-102">SYNOPSIS</span></span>
<span data-ttu-id="311ec-103">在裝置上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="311ec-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="311ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="311ec-104">SYNTAX</span></span>

### <span data-ttu-id="311ec-105">InvokeScanForUpdateParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="311ec-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-106">InvokeFsourceUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-110">InvokeFmeterUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-111">InvokeF方UpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311ec-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ec-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="311ec-114">描述</span><span class="sxs-lookup"><span data-stu-id="311ec-114">DESCRIPTION</span></span>
<span data-ttu-id="311ec-115">**Invoke-AzStackEdgeDevice Cmdlet** 會以動作來掃描、下載及安裝 Stack Edge 裝置上的更新。</span><span class="sxs-lookup"><span data-stu-id="311ec-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="311ec-116">自動掃描每天在裝置上執行，您可以執行此 Cmdlet 來明確觸發掃描。</span><span class="sxs-lookup"><span data-stu-id="311ec-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="311ec-117">例子</span><span class="sxs-lookup"><span data-stu-id="311ec-117">EXAMPLES</span></span>

### <span data-ttu-id="311ec-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="311ec-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="311ec-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="311ec-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="311ec-120">範例 3</span><span class="sxs-lookup"><span data-stu-id="311ec-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="311ec-121">參數</span><span class="sxs-lookup"><span data-stu-id="311ec-121">PARAMETERS</span></span>

### <span data-ttu-id="311ec-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="311ec-122">-AsJob</span></span>
<span data-ttu-id="311ec-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="311ec-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="311ec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311ec-124">-DefaultProfile</span></span>
<span data-ttu-id="311ec-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="311ec-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="311ec-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="311ec-126">-DeviceObject</span></span>
<span data-ttu-id="311ec-127">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="311ec-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="311ec-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="311ec-128">-FetchUpdate</span></span>
<span data-ttu-id="311ec-129">下載堆疊邊緣/閘道裝置上的更新</span><span class="sxs-lookup"><span data-stu-id="311ec-129">Downloads the updates on a Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311ec-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="311ec-130">-InstallUpdate</span></span>
<span data-ttu-id="311ec-131">在堆疊邊緣/閘道裝置上安裝更新</span><span class="sxs-lookup"><span data-stu-id="311ec-131">Installs the updates on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311ec-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="311ec-132">-Name</span></span>
<span data-ttu-id="311ec-133">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="311ec-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311ec-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="311ec-134">-PassThru</span></span>
<span data-ttu-id="311ec-135">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="311ec-135">returns true if successful</span></span>

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

### <span data-ttu-id="311ec-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311ec-136">-ResourceGroupName</span></span>
<span data-ttu-id="311ec-137">資源組名</span><span class="sxs-lookup"><span data-stu-id="311ec-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311ec-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="311ec-138">-ResourceId</span></span>
<span data-ttu-id="311ec-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="311ec-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311ec-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="311ec-140">-ScanForUpdate</span></span>
<span data-ttu-id="311ec-141">掃描堆疊邊緣/閘道裝置上的更新。</span><span class="sxs-lookup"><span data-stu-id="311ec-141">Scans for updates on a Stack edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311ec-142">-確認</span><span class="sxs-lookup"><span data-stu-id="311ec-142">-Confirm</span></span>
<span data-ttu-id="311ec-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="311ec-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="311ec-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="311ec-144">-WhatIf</span></span>
<span data-ttu-id="311ec-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="311ec-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="311ec-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="311ec-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="311ec-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311ec-147">CommonParameters</span></span>
<span data-ttu-id="311ec-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="311ec-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311ec-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="311ec-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311ec-150">輸入</span><span class="sxs-lookup"><span data-stu-id="311ec-150">INPUTS</span></span>

### <span data-ttu-id="311ec-151">沒有</span><span class="sxs-lookup"><span data-stu-id="311ec-151">None</span></span>

## <span data-ttu-id="311ec-152">輸出</span><span class="sxs-lookup"><span data-stu-id="311ec-152">OUTPUTS</span></span>

### <span data-ttu-id="311ec-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="311ec-153">System.Boolean</span></span>

## <span data-ttu-id="311ec-154">筆記</span><span class="sxs-lookup"><span data-stu-id="311ec-154">NOTES</span></span>

## <span data-ttu-id="311ec-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="311ec-155">RELATED LINKS</span></span>
