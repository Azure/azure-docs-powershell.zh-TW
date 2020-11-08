---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141732"
---
# <span data-ttu-id="59930-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="59930-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="59930-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59930-102">SYNOPSIS</span></span>
<span data-ttu-id="59930-103">在 IoT 中樞中的 IoT 裝置上取得 IoT 裝置模組或清單模組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="59930-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="59930-104">句法</span><span class="sxs-lookup"><span data-stu-id="59930-104">SYNTAX</span></span>

### <span data-ttu-id="59930-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="59930-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59930-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59930-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59930-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="59930-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59930-108">說明</span><span class="sxs-lookup"><span data-stu-id="59930-108">DESCRIPTION</span></span>
<span data-ttu-id="59930-109">在 IoT 中樞中的 IoT 裝置上取得 IoT 裝置模組或清單模組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="59930-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="59930-110">示例</span><span class="sxs-lookup"><span data-stu-id="59930-110">EXAMPLES</span></span>

### <span data-ttu-id="59930-111">範例1</span><span class="sxs-lookup"><span data-stu-id="59930-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="59930-112">在 IoT 中樞中取得 IoT 裝置模組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="59930-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="59930-113">範例2</span><span class="sxs-lookup"><span data-stu-id="59930-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="59930-114">在 IoT 中樞中的 IoT 裝置上顯示所有模組。</span><span class="sxs-lookup"><span data-stu-id="59930-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="59930-115">參數</span><span class="sxs-lookup"><span data-stu-id="59930-115">PARAMETERS</span></span>

### <span data-ttu-id="59930-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59930-116">-DefaultProfile</span></span>
<span data-ttu-id="59930-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59930-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59930-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="59930-118">-DeviceId</span></span>
<span data-ttu-id="59930-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="59930-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59930-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59930-120">-InputObject</span></span>
<span data-ttu-id="59930-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="59930-121">IotHub object</span></span>

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

### <span data-ttu-id="59930-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="59930-122">-IotHubName</span></span>
<span data-ttu-id="59930-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="59930-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="59930-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="59930-124">-ModuleId</span></span>
<span data-ttu-id="59930-125">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="59930-125">Target Module Id.</span></span>

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

### <span data-ttu-id="59930-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59930-126">-ResourceGroupName</span></span>
<span data-ttu-id="59930-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="59930-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="59930-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59930-128">-ResourceId</span></span>
<span data-ttu-id="59930-129">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="59930-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="59930-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59930-130">CommonParameters</span></span>
<span data-ttu-id="59930-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59930-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59930-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59930-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59930-133">輸入</span><span class="sxs-lookup"><span data-stu-id="59930-133">INPUTS</span></span>

### <span data-ttu-id="59930-134">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="59930-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="59930-135">System.object</span><span class="sxs-lookup"><span data-stu-id="59930-135">System.String</span></span>

## <span data-ttu-id="59930-136">輸出</span><span class="sxs-lookup"><span data-stu-id="59930-136">OUTPUTS</span></span>

### <span data-ttu-id="59930-137">PSModule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="59930-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="59930-138">PSModules []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="59930-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="59930-139">筆記</span><span class="sxs-lookup"><span data-stu-id="59930-139">NOTES</span></span>

## <span data-ttu-id="59930-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="59930-140">RELATED LINKS</span></span>
