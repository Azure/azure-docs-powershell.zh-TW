---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 07cfcacb30dd855447ab7f568cb2c1f2a61c1d75
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795766"
---
# <span data-ttu-id="b0c2b-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b0c2b-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b0c2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c2b-103">在裝置上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="b0c2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0c2b-104">SYNTAX</span></span>

### <span data-ttu-id="b0c2b-105">InvokeScanForUpdateParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b0c2b-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c2b-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0c2b-114">說明</span><span class="sxs-lookup"><span data-stu-id="b0c2b-114">DESCRIPTION</span></span>
<span data-ttu-id="b0c2b-115">**AzDataBoxEdgeDevice** Cmdlet 會呼叫 [動作]，以在 [資料] 方塊 Edge 裝置上掃描、下載及安裝更新。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="b0c2b-116">每日自動掃描會在裝置上執行，您可以執行此 Cmdlet 以明確觸發掃描。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="b0c2b-117">示例</span><span class="sxs-lookup"><span data-stu-id="b0c2b-117">EXAMPLES</span></span>

### <span data-ttu-id="b0c2b-118">範例1</span><span class="sxs-lookup"><span data-stu-id="b0c2b-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="b0c2b-119">範例2</span><span class="sxs-lookup"><span data-stu-id="b0c2b-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="b0c2b-120">範例3</span><span class="sxs-lookup"><span data-stu-id="b0c2b-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="b0c2b-121">參數</span><span class="sxs-lookup"><span data-stu-id="b0c2b-121">PARAMETERS</span></span>

### <span data-ttu-id="b0c2b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0c2b-122">-AsJob</span></span>
<span data-ttu-id="b0c2b-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0c2b-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0c2b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c2b-124">-DefaultProfile</span></span>
<span data-ttu-id="b0c2b-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0c2b-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b0c2b-126">-DeviceObject</span></span>
<span data-ttu-id="b0c2b-127">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="b0c2b-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b0c2b-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="b0c2b-128">-FetchUpdate</span></span>
<span data-ttu-id="b0c2b-129">下載資料盒 edge/閘道裝置上的更新</span><span class="sxs-lookup"><span data-stu-id="b0c2b-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="b0c2b-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="b0c2b-130">-InstallUpdate</span></span>
<span data-ttu-id="b0c2b-131">在資料盒 edge/閘道裝置上安裝更新</span><span class="sxs-lookup"><span data-stu-id="b0c2b-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="b0c2b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0c2b-132">-Name</span></span>
<span data-ttu-id="b0c2b-133">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="b0c2b-133">Device Name</span></span>

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

### <span data-ttu-id="b0c2b-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0c2b-134">-PassThru</span></span>
<span data-ttu-id="b0c2b-135">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="b0c2b-135">returns true if successful</span></span>

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

### <span data-ttu-id="b0c2b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c2b-136">-ResourceGroupName</span></span>
<span data-ttu-id="b0c2b-137">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b0c2b-137">Resource Group Name</span></span>

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

### <span data-ttu-id="b0c2b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0c2b-138">-ResourceId</span></span>
<span data-ttu-id="b0c2b-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0c2b-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="b0c2b-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="b0c2b-140">-ScanForUpdate</span></span>
<span data-ttu-id="b0c2b-141">掃描資料箱邊緣/閘道裝置上的更新。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="b0c2b-142">-確認</span><span class="sxs-lookup"><span data-stu-id="b0c2b-142">-Confirm</span></span>
<span data-ttu-id="b0c2b-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0c2b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0c2b-144">-WhatIf</span></span>
<span data-ttu-id="b0c2b-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0c2b-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0c2b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c2b-147">CommonParameters</span></span>
<span data-ttu-id="b0c2b-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c2b-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b0c2b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c2b-150">輸入</span><span class="sxs-lookup"><span data-stu-id="b0c2b-150">INPUTS</span></span>

### <span data-ttu-id="b0c2b-151">所有</span><span class="sxs-lookup"><span data-stu-id="b0c2b-151">None</span></span>

## <span data-ttu-id="b0c2b-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b0c2b-152">OUTPUTS</span></span>

### <span data-ttu-id="b0c2b-153">System.object</span><span class="sxs-lookup"><span data-stu-id="b0c2b-153">System.Boolean</span></span>

## <span data-ttu-id="b0c2b-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b0c2b-154">NOTES</span></span>

## <span data-ttu-id="b0c2b-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0c2b-155">RELATED LINKS</span></span>
