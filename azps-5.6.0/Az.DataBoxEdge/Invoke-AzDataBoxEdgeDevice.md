---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 27dc757d3a59a5ab65e30335408f38ffc19aed5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914866"
---
# <span data-ttu-id="a24e5-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a24e5-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a24e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a24e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a24e5-103">在裝置上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="a24e5-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="a24e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="a24e5-104">SYNTAX</span></span>

### <span data-ttu-id="a24e5-105">InvokeScanForUpdateParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a24e5-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-106">InvokeFsourceUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-110">InvokeFmeterUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-111">InvokeF方UpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e5-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a24e5-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a24e5-114">描述</span><span class="sxs-lookup"><span data-stu-id="a24e5-114">DESCRIPTION</span></span>
<span data-ttu-id="a24e5-115">**Invoke-AzDataBoxEdgeDevice Cmdlet** 會以動作來掃描、下載及安裝 Data Box Edge 裝置上的更新。</span><span class="sxs-lookup"><span data-stu-id="a24e5-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="a24e5-116">自動掃描每天在裝置上執行，您可以執行此 Cmdlet 來明確觸發掃描。</span><span class="sxs-lookup"><span data-stu-id="a24e5-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="a24e5-117">例子</span><span class="sxs-lookup"><span data-stu-id="a24e5-117">EXAMPLES</span></span>

### <span data-ttu-id="a24e5-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="a24e5-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="a24e5-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="a24e5-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="a24e5-120">範例 3</span><span class="sxs-lookup"><span data-stu-id="a24e5-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="a24e5-121">參數</span><span class="sxs-lookup"><span data-stu-id="a24e5-121">PARAMETERS</span></span>

### <span data-ttu-id="a24e5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a24e5-122">-AsJob</span></span>
<span data-ttu-id="a24e5-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a24e5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a24e5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24e5-124">-DefaultProfile</span></span>
<span data-ttu-id="a24e5-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a24e5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a24e5-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a24e5-126">-DeviceObject</span></span>
<span data-ttu-id="a24e5-127">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="a24e5-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24e5-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="a24e5-128">-FetchUpdate</span></span>
<span data-ttu-id="a24e5-129">在資料方塊邊緣/閘道裝置上下載更新</span><span class="sxs-lookup"><span data-stu-id="a24e5-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="a24e5-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="a24e5-130">-InstallUpdate</span></span>
<span data-ttu-id="a24e5-131">在資料方塊邊緣/閘道裝置上安裝更新</span><span class="sxs-lookup"><span data-stu-id="a24e5-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="a24e5-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="a24e5-132">-Name</span></span>
<span data-ttu-id="a24e5-133">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="a24e5-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24e5-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a24e5-134">-PassThru</span></span>
<span data-ttu-id="a24e5-135">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="a24e5-135">returns true if successful</span></span>

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

### <span data-ttu-id="a24e5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24e5-136">-ResourceGroupName</span></span>
<span data-ttu-id="a24e5-137">資源組名</span><span class="sxs-lookup"><span data-stu-id="a24e5-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24e5-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a24e5-138">-ResourceId</span></span>
<span data-ttu-id="a24e5-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a24e5-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24e5-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="a24e5-140">-ScanForUpdate</span></span>
<span data-ttu-id="a24e5-141">掃描資料方塊邊緣/閘道裝置上的更新。</span><span class="sxs-lookup"><span data-stu-id="a24e5-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="a24e5-142">-確認</span><span class="sxs-lookup"><span data-stu-id="a24e5-142">-Confirm</span></span>
<span data-ttu-id="a24e5-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a24e5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a24e5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24e5-144">-WhatIf</span></span>
<span data-ttu-id="a24e5-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a24e5-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a24e5-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a24e5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a24e5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24e5-147">CommonParameters</span></span>
<span data-ttu-id="a24e5-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a24e5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24e5-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a24e5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24e5-150">輸入</span><span class="sxs-lookup"><span data-stu-id="a24e5-150">INPUTS</span></span>

### <span data-ttu-id="a24e5-151">沒有</span><span class="sxs-lookup"><span data-stu-id="a24e5-151">None</span></span>

## <span data-ttu-id="a24e5-152">輸出</span><span class="sxs-lookup"><span data-stu-id="a24e5-152">OUTPUTS</span></span>

### <span data-ttu-id="a24e5-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a24e5-153">System.Boolean</span></span>

## <span data-ttu-id="a24e5-154">筆記</span><span class="sxs-lookup"><span data-stu-id="a24e5-154">NOTES</span></span>

## <span data-ttu-id="a24e5-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="a24e5-155">RELATED LINKS</span></span>
