---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136463"
---
# <span data-ttu-id="f9b74-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f9b74-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f9b74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9b74-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b74-103">在裝置上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="f9b74-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="f9b74-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9b74-104">SYNTAX</span></span>

### <span data-ttu-id="f9b74-105">InvokeScanForUpdateParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9b74-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b74-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b74-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b74-114">說明</span><span class="sxs-lookup"><span data-stu-id="f9b74-114">DESCRIPTION</span></span>
<span data-ttu-id="f9b74-115">**AzDataBoxEdgeDevice** Cmdlet 會呼叫 [動作]，以在 [資料] 方塊 Edge 裝置上掃描、下載及安裝更新。</span><span class="sxs-lookup"><span data-stu-id="f9b74-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="f9b74-116">每日自動掃描會在裝置上執行，您可以執行此 Cmdlet 以明確觸發掃描。</span><span class="sxs-lookup"><span data-stu-id="f9b74-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="f9b74-117">示例</span><span class="sxs-lookup"><span data-stu-id="f9b74-117">EXAMPLES</span></span>

### <span data-ttu-id="f9b74-118">範例1</span><span class="sxs-lookup"><span data-stu-id="f9b74-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="f9b74-119">範例2</span><span class="sxs-lookup"><span data-stu-id="f9b74-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="f9b74-120">範例3</span><span class="sxs-lookup"><span data-stu-id="f9b74-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="f9b74-121">參數</span><span class="sxs-lookup"><span data-stu-id="f9b74-121">PARAMETERS</span></span>

### <span data-ttu-id="f9b74-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9b74-122">-AsJob</span></span>
<span data-ttu-id="f9b74-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9b74-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9b74-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b74-124">-DefaultProfile</span></span>
<span data-ttu-id="f9b74-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9b74-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b74-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f9b74-126">-DeviceObject</span></span>
<span data-ttu-id="f9b74-127">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="f9b74-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="f9b74-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="f9b74-128">-FetchUpdate</span></span>
<span data-ttu-id="f9b74-129">下載資料盒 edge/閘道裝置上的更新</span><span class="sxs-lookup"><span data-stu-id="f9b74-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="f9b74-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="f9b74-130">-InstallUpdate</span></span>
<span data-ttu-id="f9b74-131">在資料盒 edge/閘道裝置上安裝更新</span><span class="sxs-lookup"><span data-stu-id="f9b74-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="f9b74-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9b74-132">-Name</span></span>
<span data-ttu-id="f9b74-133">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="f9b74-133">Device Name</span></span>

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

### <span data-ttu-id="f9b74-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9b74-134">-PassThru</span></span>
<span data-ttu-id="f9b74-135">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="f9b74-135">returns true if successful</span></span>

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

### <span data-ttu-id="f9b74-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b74-136">-ResourceGroupName</span></span>
<span data-ttu-id="f9b74-137">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f9b74-137">Resource Group Name</span></span>

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

### <span data-ttu-id="f9b74-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9b74-138">-ResourceId</span></span>
<span data-ttu-id="f9b74-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9b74-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="f9b74-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="f9b74-140">-ScanForUpdate</span></span>
<span data-ttu-id="f9b74-141">掃描資料箱邊緣/閘道裝置上的更新。</span><span class="sxs-lookup"><span data-stu-id="f9b74-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="f9b74-142">-確認</span><span class="sxs-lookup"><span data-stu-id="f9b74-142">-Confirm</span></span>
<span data-ttu-id="f9b74-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9b74-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b74-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b74-144">-WhatIf</span></span>
<span data-ttu-id="f9b74-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9b74-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9b74-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9b74-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b74-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b74-147">CommonParameters</span></span>
<span data-ttu-id="f9b74-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9b74-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b74-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9b74-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b74-150">輸入</span><span class="sxs-lookup"><span data-stu-id="f9b74-150">INPUTS</span></span>

### <span data-ttu-id="f9b74-151">所有</span><span class="sxs-lookup"><span data-stu-id="f9b74-151">None</span></span>

## <span data-ttu-id="f9b74-152">輸出</span><span class="sxs-lookup"><span data-stu-id="f9b74-152">OUTPUTS</span></span>

### <span data-ttu-id="f9b74-153">System.object</span><span class="sxs-lookup"><span data-stu-id="f9b74-153">System.Boolean</span></span>

## <span data-ttu-id="f9b74-154">筆記</span><span class="sxs-lookup"><span data-stu-id="f9b74-154">NOTES</span></span>

## <span data-ttu-id="f9b74-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9b74-155">RELATED LINKS</span></span>
