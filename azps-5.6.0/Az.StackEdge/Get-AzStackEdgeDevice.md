---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: dbc5e0bf327383adafa980d3475d196173fa0fdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916857"
---
# <span data-ttu-id="962cd-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="962cd-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="962cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="962cd-102">SYNOPSIS</span></span>
<span data-ttu-id="962cd-103">在可用的 Stack Edge 裝置上獲得資訊。</span><span class="sxs-lookup"><span data-stu-id="962cd-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="962cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="962cd-104">SYNTAX</span></span>

### <span data-ttu-id="962cd-105">ListByParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="962cd-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="962cd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="962cd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="962cd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="962cd-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="962cd-108">描述</span><span class="sxs-lookup"><span data-stu-id="962cd-108">DESCRIPTION</span></span>
<span data-ttu-id="962cd-109">**Get-AzStackEdgeDevice Cmdlet** 會取得可用 Stack Edge 裝置的資訊。</span><span class="sxs-lookup"><span data-stu-id="962cd-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="962cd-110">您可以指定裝置名稱以及資源組名，以取得特定裝置上的資訊。</span><span class="sxs-lookup"><span data-stu-id="962cd-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="962cd-111">例子</span><span class="sxs-lookup"><span data-stu-id="962cd-111">EXAMPLES</span></span>

### <span data-ttu-id="962cd-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="962cd-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="962cd-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="962cd-113">Example 2</span></span>
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

## <span data-ttu-id="962cd-114">參數</span><span class="sxs-lookup"><span data-stu-id="962cd-114">PARAMETERS</span></span>

### <span data-ttu-id="962cd-115">-警示</span><span class="sxs-lookup"><span data-stu-id="962cd-115">-Alert</span></span>
<span data-ttu-id="962cd-116">在堆疊邊緣/閘道裝置上抓取通知</span><span class="sxs-lookup"><span data-stu-id="962cd-116">Fetch the alerts on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="962cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962cd-117">-DefaultProfile</span></span>
<span data-ttu-id="962cd-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="962cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="962cd-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="962cd-119">-ExtendedInfo</span></span>
<span data-ttu-id="962cd-120">為指定的 Stack Edge/Stack 閘道裝置獲得其他資訊</span><span class="sxs-lookup"><span data-stu-id="962cd-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

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

### <span data-ttu-id="962cd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="962cd-121">-Name</span></span>
<span data-ttu-id="962cd-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="962cd-122">Resource Group Name</span></span>

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

### <span data-ttu-id="962cd-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="962cd-123">-NetworkSetting</span></span>
<span data-ttu-id="962cd-124">獲得指定 Stack Edge/Stack 閘道裝置的網路設定</span><span class="sxs-lookup"><span data-stu-id="962cd-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

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

### <span data-ttu-id="962cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="962cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="962cd-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="962cd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="962cd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="962cd-127">-ResourceId</span></span>
<span data-ttu-id="962cd-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="962cd-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="962cd-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="962cd-129">-UpdateSummary</span></span>
<span data-ttu-id="962cd-130">根據裝置的最後一次掃描，獲得更新可用性的資訊。</span><span class="sxs-lookup"><span data-stu-id="962cd-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="962cd-131">它也會獲得裝置上任何持續下載或安裝工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="962cd-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="962cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962cd-132">CommonParameters</span></span>
<span data-ttu-id="962cd-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="962cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962cd-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="962cd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962cd-135">輸入</span><span class="sxs-lookup"><span data-stu-id="962cd-135">INPUTS</span></span>

## <span data-ttu-id="962cd-136">輸出</span><span class="sxs-lookup"><span data-stu-id="962cd-136">OUTPUTS</span></span>

## <span data-ttu-id="962cd-137">筆記</span><span class="sxs-lookup"><span data-stu-id="962cd-137">NOTES</span></span>

## <span data-ttu-id="962cd-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="962cd-138">RELATED LINKS</span></span>
