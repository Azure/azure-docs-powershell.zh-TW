---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141735"
---
# <span data-ttu-id="c4878-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="c4878-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="c4878-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4878-102">SYNOPSIS</span></span>
<span data-ttu-id="c4878-103">取得裝置的分散式追蹤設定。</span><span class="sxs-lookup"><span data-stu-id="c4878-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c4878-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4878-104">SYNTAX</span></span>

### <span data-ttu-id="c4878-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c4878-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4878-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c4878-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4878-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c4878-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4878-108">說明</span><span class="sxs-lookup"><span data-stu-id="c4878-108">DESCRIPTION</span></span>
<span data-ttu-id="c4878-109">取得裝置的分散式追蹤設定。</span><span class="sxs-lookup"><span data-stu-id="c4878-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c4878-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4878-110">EXAMPLES</span></span>

### <span data-ttu-id="c4878-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c4878-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="c4878-112">取得裝置的分散式追蹤設定。</span><span class="sxs-lookup"><span data-stu-id="c4878-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c4878-113">參數</span><span class="sxs-lookup"><span data-stu-id="c4878-113">PARAMETERS</span></span>

### <span data-ttu-id="c4878-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4878-114">-DefaultProfile</span></span>
<span data-ttu-id="c4878-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4878-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4878-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c4878-116">-DeviceId</span></span>
<span data-ttu-id="c4878-117">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4878-117">Target Device Id.</span></span>

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

### <span data-ttu-id="c4878-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4878-118">-InputObject</span></span>
<span data-ttu-id="c4878-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c4878-119">IotHub object</span></span>

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

### <span data-ttu-id="c4878-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c4878-120">-IotHubName</span></span>
<span data-ttu-id="c4878-121">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="c4878-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c4878-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4878-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4878-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c4878-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c4878-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4878-124">-ResourceId</span></span>
<span data-ttu-id="c4878-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c4878-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c4878-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4878-126">CommonParameters</span></span>
<span data-ttu-id="c4878-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4878-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4878-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4878-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4878-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c4878-129">INPUTS</span></span>

### <span data-ttu-id="c4878-130">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="c4878-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c4878-131">System.object</span><span class="sxs-lookup"><span data-stu-id="c4878-131">System.String</span></span>

## <span data-ttu-id="c4878-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c4878-132">OUTPUTS</span></span>

### <span data-ttu-id="c4878-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="c4878-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="c4878-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c4878-134">NOTES</span></span>

## <span data-ttu-id="c4878-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4878-135">RELATED LINKS</span></span>
