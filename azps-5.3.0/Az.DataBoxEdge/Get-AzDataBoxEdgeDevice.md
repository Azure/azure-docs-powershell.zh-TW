---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439632"
---
# <span data-ttu-id="155ba-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="155ba-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="155ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="155ba-102">SYNOPSIS</span></span>
<span data-ttu-id="155ba-103">取得可用資料編輯方塊邊緣裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="155ba-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="155ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="155ba-104">SYNTAX</span></span>

### <span data-ttu-id="155ba-105">ListByParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="155ba-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="155ba-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="155ba-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="155ba-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="155ba-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="155ba-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="155ba-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="155ba-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="155ba-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="155ba-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="155ba-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ba-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="155ba-116">說明</span><span class="sxs-lookup"><span data-stu-id="155ba-116">DESCRIPTION</span></span>
<span data-ttu-id="155ba-117">**AzDataBoxEdgeDevice** Cmdlet 會取得可用資料盒 Edge 裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="155ba-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="155ba-118">您可以指定裝置的名稱以及資源群組名稱，以取得特定裝置上的資訊。</span><span class="sxs-lookup"><span data-stu-id="155ba-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="155ba-119">示例</span><span class="sxs-lookup"><span data-stu-id="155ba-119">EXAMPLES</span></span>

### <span data-ttu-id="155ba-120">範例1</span><span class="sxs-lookup"><span data-stu-id="155ba-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="155ba-121">範例2</span><span class="sxs-lookup"><span data-stu-id="155ba-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="155ba-122">範例3</span><span class="sxs-lookup"><span data-stu-id="155ba-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="155ba-123">參數</span><span class="sxs-lookup"><span data-stu-id="155ba-123">PARAMETERS</span></span>

### <span data-ttu-id="155ba-124">-提醒</span><span class="sxs-lookup"><span data-stu-id="155ba-124">-Alert</span></span>
<span data-ttu-id="155ba-125">取得資料盒 edge/閘道裝置上的通知</span><span class="sxs-lookup"><span data-stu-id="155ba-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155ba-126">-DefaultProfile</span></span>
<span data-ttu-id="155ba-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="155ba-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="155ba-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="155ba-128">-ExtendedInfo</span></span>
<span data-ttu-id="155ba-129">取得指定資料方塊 Edge/資料編輯方塊裝置的其他資訊</span><span class="sxs-lookup"><span data-stu-id="155ba-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ba-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="155ba-130">-Name</span></span>
<span data-ttu-id="155ba-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="155ba-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ba-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="155ba-132">-NetworkSetting</span></span>
<span data-ttu-id="155ba-133">取得指定資料盒 Edge/資料盒裝置的網路設定</span><span class="sxs-lookup"><span data-stu-id="155ba-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ba-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155ba-134">-ResourceGroupName</span></span>
<span data-ttu-id="155ba-135">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="155ba-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ba-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="155ba-136">-ResourceId</span></span>
<span data-ttu-id="155ba-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="155ba-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ba-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="155ba-138">-UpdateSummary</span></span>
<span data-ttu-id="155ba-139">根據裝置的上次掃描，取得更新可用性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="155ba-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="155ba-140">它也會取得有關裝置上任何正在進行的下載或安裝作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="155ba-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ba-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155ba-141">CommonParameters</span></span>
<span data-ttu-id="155ba-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="155ba-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155ba-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="155ba-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155ba-144">輸入</span><span class="sxs-lookup"><span data-stu-id="155ba-144">INPUTS</span></span>

### <span data-ttu-id="155ba-145">所有</span><span class="sxs-lookup"><span data-stu-id="155ba-145">None</span></span>

## <span data-ttu-id="155ba-146">輸出</span><span class="sxs-lookup"><span data-stu-id="155ba-146">OUTPUTS</span></span>

### <span data-ttu-id="155ba-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="155ba-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="155ba-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="155ba-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="155ba-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="155ba-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="155ba-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="155ba-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="155ba-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="155ba-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="155ba-152">筆記</span><span class="sxs-lookup"><span data-stu-id="155ba-152">NOTES</span></span>

## <span data-ttu-id="155ba-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="155ba-153">RELATED LINKS</span></span>
