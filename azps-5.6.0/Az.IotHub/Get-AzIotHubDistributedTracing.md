---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: 290b2ddcea6812b840b9c19ad2d44c4a0e461e64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911058"
---
# <span data-ttu-id="fbdc8-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="fbdc8-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="fbdc8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fbdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdc8-103">取得裝置分散式追蹤設定。</span><span class="sxs-lookup"><span data-stu-id="fbdc8-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fbdc8-104">語法</span><span class="sxs-lookup"><span data-stu-id="fbdc8-104">SYNTAX</span></span>

### <span data-ttu-id="fbdc8-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fbdc8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbdc8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fbdc8-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbdc8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fbdc8-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbdc8-108">描述</span><span class="sxs-lookup"><span data-stu-id="fbdc8-108">DESCRIPTION</span></span>
<span data-ttu-id="fbdc8-109">取得裝置分散式追蹤設定。</span><span class="sxs-lookup"><span data-stu-id="fbdc8-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fbdc8-110">例子</span><span class="sxs-lookup"><span data-stu-id="fbdc8-110">EXAMPLES</span></span>

### <span data-ttu-id="fbdc8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="fbdc8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="fbdc8-112">取得裝置分散式追蹤設定。</span><span class="sxs-lookup"><span data-stu-id="fbdc8-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fbdc8-113">參數</span><span class="sxs-lookup"><span data-stu-id="fbdc8-113">PARAMETERS</span></span>

### <span data-ttu-id="fbdc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdc8-114">-DefaultProfile</span></span>
<span data-ttu-id="fbdc8-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fbdc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbdc8-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fbdc8-116">-DeviceId</span></span>
<span data-ttu-id="fbdc8-117">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbdc8-117">Target Device Id.</span></span>

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

### <span data-ttu-id="fbdc8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbdc8-118">-InputObject</span></span>
<span data-ttu-id="fbdc8-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="fbdc8-119">IotHub object</span></span>

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

### <span data-ttu-id="fbdc8-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fbdc8-120">-IotHubName</span></span>
<span data-ttu-id="fbdc8-121">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="fbdc8-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fbdc8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbdc8-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbdc8-123">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="fbdc8-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fbdc8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbdc8-124">-ResourceId</span></span>
<span data-ttu-id="fbdc8-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fbdc8-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fbdc8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdc8-126">CommonParameters</span></span>
<span data-ttu-id="fbdc8-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fbdc8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdc8-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fbdc8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdc8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fbdc8-129">INPUTS</span></span>

### <span data-ttu-id="fbdc8-130">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fbdc8-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fbdc8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fbdc8-131">System.String</span></span>

## <span data-ttu-id="fbdc8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fbdc8-132">OUTPUTS</span></span>

### <span data-ttu-id="fbdc8-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDMicrosoft.Azure.Commands.Management.IotHub.Models.PSD追蹤</span><span class="sxs-lookup"><span data-stu-id="fbdc8-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="fbdc8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fbdc8-134">NOTES</span></span>

## <span data-ttu-id="fbdc8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbdc8-135">RELATED LINKS</span></span>
