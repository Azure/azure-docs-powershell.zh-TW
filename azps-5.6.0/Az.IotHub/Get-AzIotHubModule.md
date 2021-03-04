---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: c2515ff590543c448985f0c6635278430d8ae63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911038"
---
# <span data-ttu-id="e7a22-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="e7a22-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="e7a22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7a22-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a22-103">取得位於 IoT 中心 IoT 裝置上的 IoT 裝置模組或清單模組詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e7a22-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e7a22-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7a22-104">SYNTAX</span></span>

### <span data-ttu-id="e7a22-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e7a22-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7a22-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e7a22-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7a22-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e7a22-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a22-108">描述</span><span class="sxs-lookup"><span data-stu-id="e7a22-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a22-109">取得位於 IoT 中心 IoT 裝置上的 IoT 裝置模組或清單模組詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e7a22-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e7a22-110">例子</span><span class="sxs-lookup"><span data-stu-id="e7a22-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a22-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e7a22-111">Example 1</span></span>
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

<span data-ttu-id="e7a22-112">取得 IoT 中心中 IoT 裝置模組的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e7a22-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="e7a22-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="e7a22-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="e7a22-114">顯示位於 IoT 中心 IoT 裝置上的所有模組。</span><span class="sxs-lookup"><span data-stu-id="e7a22-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e7a22-115">參數</span><span class="sxs-lookup"><span data-stu-id="e7a22-115">PARAMETERS</span></span>

### <span data-ttu-id="e7a22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a22-116">-DefaultProfile</span></span>
<span data-ttu-id="e7a22-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7a22-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a22-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e7a22-118">-DeviceId</span></span>
<span data-ttu-id="e7a22-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7a22-119">Target Device Id.</span></span>

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

### <span data-ttu-id="e7a22-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a22-120">-InputObject</span></span>
<span data-ttu-id="e7a22-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="e7a22-121">IotHub object</span></span>

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

### <span data-ttu-id="e7a22-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e7a22-122">-IotHubName</span></span>
<span data-ttu-id="e7a22-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="e7a22-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e7a22-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="e7a22-124">-ModuleId</span></span>
<span data-ttu-id="e7a22-125">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7a22-125">Target Module Id.</span></span>

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

### <span data-ttu-id="e7a22-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a22-126">-ResourceGroupName</span></span>
<span data-ttu-id="e7a22-127">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="e7a22-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e7a22-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a22-128">-ResourceId</span></span>
<span data-ttu-id="e7a22-129">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e7a22-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e7a22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a22-130">CommonParameters</span></span>
<span data-ttu-id="e7a22-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7a22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a22-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e7a22-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a22-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e7a22-133">INPUTS</span></span>

### <span data-ttu-id="e7a22-134">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e7a22-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e7a22-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e7a22-135">System.String</span></span>

## <span data-ttu-id="e7a22-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e7a22-136">OUTPUTS</span></span>

### <span data-ttu-id="e7a22-137">Microsoft.Azure.Commands.management.IotHub.models.PSModule</span><span class="sxs-lookup"><span data-stu-id="e7a22-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="e7a22-138">Microsoft.Azure.Commands.management.IotHub.models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="e7a22-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="e7a22-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e7a22-139">NOTES</span></span>

## <span data-ttu-id="e7a22-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7a22-140">RELATED LINKS</span></span>
