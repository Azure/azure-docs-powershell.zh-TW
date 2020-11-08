---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129308"
---
# <span data-ttu-id="1dbe3-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1dbe3-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="1dbe3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbe3-103">列出 Azure IoT 中樞中包含的所有裝置或特定裝置。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="1dbe3-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dbe3-104">SYNTAX</span></span>

### <span data-ttu-id="1dbe3-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1dbe3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbe3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1dbe3-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dbe3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1dbe3-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbe3-108">說明</span><span class="sxs-lookup"><span data-stu-id="1dbe3-108">DESCRIPTION</span></span>
<span data-ttu-id="1dbe3-109">取得 iot 中心裝置的詳細資料，或列出 Iot 中樞中的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="1dbe3-110">示例</span><span class="sxs-lookup"><span data-stu-id="1dbe3-110">EXAMPLES</span></span>

### <span data-ttu-id="1dbe3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1dbe3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="1dbe3-112">顯示 Iot 中樞中的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="1dbe3-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1dbe3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="1dbe3-114">取得 IoT 中心裝置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="1dbe3-115">參數</span><span class="sxs-lookup"><span data-stu-id="1dbe3-115">PARAMETERS</span></span>

### <span data-ttu-id="1dbe3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbe3-116">-DefaultProfile</span></span>
<span data-ttu-id="1dbe3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbe3-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1dbe3-118">-DeviceId</span></span>
<span data-ttu-id="1dbe3-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dbe3-120">-InputObject</span></span>
<span data-ttu-id="1dbe3-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="1dbe3-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe3-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1dbe3-122">-IotHubName</span></span>
<span data-ttu-id="1dbe3-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="1dbe3-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbe3-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dbe3-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="1dbe3-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dbe3-126">-ResourceId</span></span>
<span data-ttu-id="1dbe3-127">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1dbe3-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbe3-128">CommonParameters</span></span>
<span data-ttu-id="1dbe3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbe3-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbe3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1dbe3-131">INPUTS</span></span>

### <span data-ttu-id="1dbe3-132">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="1dbe3-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1dbe3-133">System.object</span><span class="sxs-lookup"><span data-stu-id="1dbe3-133">System.String</span></span>

## <span data-ttu-id="1dbe3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1dbe3-134">OUTPUTS</span></span>

### <span data-ttu-id="1dbe3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="1dbe3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="1dbe3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices []</span><span class="sxs-lookup"><span data-stu-id="1dbe3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="1dbe3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1dbe3-137">NOTES</span></span>

## <span data-ttu-id="1dbe3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dbe3-138">RELATED LINKS</span></span>