---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: 1fa868d9df41a5f4f995981c332497d9555e1174
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126739"
---
# <span data-ttu-id="43442-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="43442-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="43442-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43442-102">SYNOPSIS</span></span>
<span data-ttu-id="43442-103">取得可用堆疊邊緣裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="43442-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="43442-104">句法</span><span class="sxs-lookup"><span data-stu-id="43442-104">SYNTAX</span></span>

### <span data-ttu-id="43442-105">ListByParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43442-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43442-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43442-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43442-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43442-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43442-108">說明</span><span class="sxs-lookup"><span data-stu-id="43442-108">DESCRIPTION</span></span>
<span data-ttu-id="43442-109">**AzStackEdgeDevice** Cmdlet 會取得可用堆疊邊緣裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="43442-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="43442-110">您可以指定裝置的名稱以及資源群組名稱，以取得特定裝置上的資訊。</span><span class="sxs-lookup"><span data-stu-id="43442-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="43442-111">示例</span><span class="sxs-lookup"><span data-stu-id="43442-111">EXAMPLES</span></span>

### <span data-ttu-id="43442-112">範例1</span><span class="sxs-lookup"><span data-stu-id="43442-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="43442-113">範例2</span><span class="sxs-lookup"><span data-stu-id="43442-113">Example 2</span></span>
```powershell
PS C:\>$device = Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName1 -DeviceName deviceNameOne -Alert -UpdateSummary -NetworkSetting -ExtendedInfo

PS C:\>$device.Alert

Title                            Severity AppearedDateTime      Recommendation
-----                            -------- ----------------      --------------
Lost heartbeat from your device. Critical 02-Jan-20 10:35:20 AM If your device is offline, then the device is not able to communicate with the Azure service. This could be due to one of the following reasons: <br/> &nbs�


PS C:\>$device.NetworkSetting

State    IPv4         IPv6                                 Subnet        Default Gateway Physical address DNS Servers
-----    ----         ----                                 ------        --------------- ---------------- -----------
Disabled 10.150.76.82 2404:f801:4800:1e:8168:dca6:b3b9:d70 255.255.252.0 10.150.76.1     00155D4E262B     10.50.50.50,10.50.10.50

PS C:\>$device.UpdateSummary

DeviceName        Current Version Friendly name      Last Software Scan Last Software Update Pending Updates Pending Update Titles
----------        --------------- -------------      ------------------ -------------------- --------------- ---------------------
deviceNameOne     2.0.998.537     Data Box Edge Mock                                         0

PS C:\>$device.ExtendedInfo

ResourceGroupName   DeviceName        EncryptedCIK Thumbprint     ResourceKey        EncryptedCIK
-----------------   ----------        -----------------------     -----------        ------------
resourceGroupName1  deviceNameOne     EncryptedCIKThumbpring      411182691329779166 EncryptedCIK
```

## <span data-ttu-id="43442-114">參數</span><span class="sxs-lookup"><span data-stu-id="43442-114">PARAMETERS</span></span>

### <span data-ttu-id="43442-115">-提醒</span><span class="sxs-lookup"><span data-stu-id="43442-115">-Alert</span></span>
<span data-ttu-id="43442-116">在堆疊 edge/閘道裝置上提取警報</span><span class="sxs-lookup"><span data-stu-id="43442-116">Fetch the alerts on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43442-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43442-117">-DefaultProfile</span></span>
<span data-ttu-id="43442-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43442-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43442-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="43442-119">-ExtendedInfo</span></span>
<span data-ttu-id="43442-120">取得指定堆疊邊緣/堆疊閘道裝置的其他資訊</span><span class="sxs-lookup"><span data-stu-id="43442-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43442-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="43442-121">-Name</span></span>
<span data-ttu-id="43442-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43442-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43442-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="43442-123">-NetworkSetting</span></span>
<span data-ttu-id="43442-124">取得指定堆疊邊緣/堆疊閘道裝置的網路設定</span><span class="sxs-lookup"><span data-stu-id="43442-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43442-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43442-125">-ResourceGroupName</span></span>
<span data-ttu-id="43442-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43442-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43442-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43442-127">-ResourceId</span></span>
<span data-ttu-id="43442-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="43442-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43442-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="43442-129">-UpdateSummary</span></span>
<span data-ttu-id="43442-130">根據裝置的上次掃描，取得更新可用性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="43442-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="43442-131">它也會取得有關裝置上任何正在進行的下載或安裝作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="43442-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43442-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43442-132">CommonParameters</span></span>
<span data-ttu-id="43442-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43442-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43442-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43442-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43442-135">輸入</span><span class="sxs-lookup"><span data-stu-id="43442-135">INPUTS</span></span>

## <span data-ttu-id="43442-136">輸出</span><span class="sxs-lookup"><span data-stu-id="43442-136">OUTPUTS</span></span>

## <span data-ttu-id="43442-137">筆記</span><span class="sxs-lookup"><span data-stu-id="43442-137">NOTES</span></span>

## <span data-ttu-id="43442-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="43442-138">RELATED LINKS</span></span>
