---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956987"
---
# <span data-ttu-id="862fd-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="862fd-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="862fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="862fd-102">SYNOPSIS</span></span>
<span data-ttu-id="862fd-103">在裝置上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="862fd-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="862fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="862fd-104">SYNTAX</span></span>

### <span data-ttu-id="862fd-105">InvokeScanForUpdateParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="862fd-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862fd-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="862fd-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="862fd-114">說明</span><span class="sxs-lookup"><span data-stu-id="862fd-114">DESCRIPTION</span></span>
<span data-ttu-id="862fd-115">**AzStackEdgeDevice** Cmdlet 會呼叫要在堆疊 Edge 裝置上掃描、下載及安裝更新的動作。</span><span class="sxs-lookup"><span data-stu-id="862fd-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="862fd-116">每日自動掃描會在裝置上執行，您可以執行此 Cmdlet 以明確觸發掃描。</span><span class="sxs-lookup"><span data-stu-id="862fd-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="862fd-117">示例</span><span class="sxs-lookup"><span data-stu-id="862fd-117">EXAMPLES</span></span>

### <span data-ttu-id="862fd-118">範例1</span><span class="sxs-lookup"><span data-stu-id="862fd-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="862fd-119">範例2</span><span class="sxs-lookup"><span data-stu-id="862fd-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="862fd-120">範例3</span><span class="sxs-lookup"><span data-stu-id="862fd-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="862fd-121">參數</span><span class="sxs-lookup"><span data-stu-id="862fd-121">PARAMETERS</span></span>

### <span data-ttu-id="862fd-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="862fd-122">-AsJob</span></span>
<span data-ttu-id="862fd-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="862fd-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="862fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862fd-124">-DefaultProfile</span></span>
<span data-ttu-id="862fd-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="862fd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="862fd-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="862fd-126">-DeviceObject</span></span>
<span data-ttu-id="862fd-127">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="862fd-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="862fd-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="862fd-128">-FetchUpdate</span></span>
<span data-ttu-id="862fd-129">下載堆疊 edge/閘道裝置上的更新</span><span class="sxs-lookup"><span data-stu-id="862fd-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="862fd-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="862fd-130">-InstallUpdate</span></span>
<span data-ttu-id="862fd-131">在堆疊 edge/閘道裝置上安裝更新</span><span class="sxs-lookup"><span data-stu-id="862fd-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="862fd-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="862fd-132">-Name</span></span>
<span data-ttu-id="862fd-133">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="862fd-133">Device Name</span></span>

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

### <span data-ttu-id="862fd-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="862fd-134">-PassThru</span></span>
<span data-ttu-id="862fd-135">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="862fd-135">returns true if successful</span></span>

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

### <span data-ttu-id="862fd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="862fd-136">-ResourceGroupName</span></span>
<span data-ttu-id="862fd-137">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="862fd-137">Resource Group Name</span></span>

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

### <span data-ttu-id="862fd-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="862fd-138">-ResourceId</span></span>
<span data-ttu-id="862fd-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="862fd-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="862fd-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="862fd-140">-ScanForUpdate</span></span>
<span data-ttu-id="862fd-141">掃描堆疊 edge/閘道裝置上的更新。</span><span class="sxs-lookup"><span data-stu-id="862fd-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="862fd-142">-確認</span><span class="sxs-lookup"><span data-stu-id="862fd-142">-Confirm</span></span>
<span data-ttu-id="862fd-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="862fd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="862fd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="862fd-144">-WhatIf</span></span>
<span data-ttu-id="862fd-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="862fd-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="862fd-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="862fd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="862fd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862fd-147">CommonParameters</span></span>
<span data-ttu-id="862fd-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="862fd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862fd-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="862fd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862fd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="862fd-150">INPUTS</span></span>

### <span data-ttu-id="862fd-151">所有</span><span class="sxs-lookup"><span data-stu-id="862fd-151">None</span></span>

## <span data-ttu-id="862fd-152">輸出</span><span class="sxs-lookup"><span data-stu-id="862fd-152">OUTPUTS</span></span>

### <span data-ttu-id="862fd-153">System.object</span><span class="sxs-lookup"><span data-stu-id="862fd-153">System.Boolean</span></span>

## <span data-ttu-id="862fd-154">筆記</span><span class="sxs-lookup"><span data-stu-id="862fd-154">NOTES</span></span>

## <span data-ttu-id="862fd-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="862fd-155">RELATED LINKS</span></span>
