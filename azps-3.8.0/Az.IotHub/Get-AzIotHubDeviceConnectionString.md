---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958942"
---
# <span data-ttu-id="6beb6-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="6beb6-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="6beb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6beb6-102">SYNOPSIS</span></span>
<span data-ttu-id="6beb6-103">在 Iot 中樞中取得目標 IoT 裝置的連線字串。</span><span class="sxs-lookup"><span data-stu-id="6beb6-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="6beb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6beb6-104">SYNTAX</span></span>

### <span data-ttu-id="6beb6-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6beb6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6beb6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6beb6-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6beb6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6beb6-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6beb6-108">說明</span><span class="sxs-lookup"><span data-stu-id="6beb6-108">DESCRIPTION</span></span>
<span data-ttu-id="6beb6-109">列出 Azure IoT 中樞中包含的所有裝置或目標 IoT 裝置的連線字串。</span><span class="sxs-lookup"><span data-stu-id="6beb6-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="6beb6-110">示例</span><span class="sxs-lookup"><span data-stu-id="6beb6-110">EXAMPLES</span></span>

### <span data-ttu-id="6beb6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6beb6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="6beb6-112">顯示 Iot 中樞中的所有裝置連線字串。</span><span class="sxs-lookup"><span data-stu-id="6beb6-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="6beb6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="6beb6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="6beb6-114">取得 IoT 裝置的次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="6beb6-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="6beb6-115">參數</span><span class="sxs-lookup"><span data-stu-id="6beb6-115">PARAMETERS</span></span>

### <span data-ttu-id="6beb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beb6-116">-DefaultProfile</span></span>
<span data-ttu-id="6beb6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6beb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6beb6-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6beb6-118">-DeviceId</span></span>
<span data-ttu-id="6beb6-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6beb6-119">Target Device Id.</span></span>

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

### <span data-ttu-id="6beb6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6beb6-120">-InputObject</span></span>
<span data-ttu-id="6beb6-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="6beb6-121">IotHub object</span></span>

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

### <span data-ttu-id="6beb6-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6beb6-122">-IotHubName</span></span>
<span data-ttu-id="6beb6-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="6beb6-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6beb6-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6beb6-124">-KeyType</span></span>
<span data-ttu-id="6beb6-125">Auth 的共用存取原則金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="6beb6-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6beb6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6beb6-126">-ResourceGroupName</span></span>
<span data-ttu-id="6beb6-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6beb6-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6beb6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6beb6-128">-ResourceId</span></span>
<span data-ttu-id="6beb6-129">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6beb6-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6beb6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beb6-130">CommonParameters</span></span>
<span data-ttu-id="6beb6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6beb6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beb6-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6beb6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beb6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6beb6-133">INPUTS</span></span>

### <span data-ttu-id="6beb6-134">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="6beb6-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6beb6-135">System.object</span><span class="sxs-lookup"><span data-stu-id="6beb6-135">System.String</span></span>

## <span data-ttu-id="6beb6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6beb6-136">OUTPUTS</span></span>

### <span data-ttu-id="6beb6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="6beb6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="6beb6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6beb6-138">NOTES</span></span>

## <span data-ttu-id="6beb6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6beb6-139">RELATED LINKS</span></span>