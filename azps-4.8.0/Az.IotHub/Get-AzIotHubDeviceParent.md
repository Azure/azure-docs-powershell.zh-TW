---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127912"
---
# <span data-ttu-id="74a21-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="74a21-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="74a21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74a21-102">SYNOPSIS</span></span>
<span data-ttu-id="74a21-103">取得指定裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="74a21-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="74a21-104">句法</span><span class="sxs-lookup"><span data-stu-id="74a21-104">SYNTAX</span></span>

### <span data-ttu-id="74a21-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74a21-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74a21-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="74a21-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74a21-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="74a21-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74a21-108">說明</span><span class="sxs-lookup"><span data-stu-id="74a21-108">DESCRIPTION</span></span>
<span data-ttu-id="74a21-109">取得指定非邊緣裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="74a21-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="74a21-110">示例</span><span class="sxs-lookup"><span data-stu-id="74a21-110">EXAMPLES</span></span>

### <span data-ttu-id="74a21-111">範例1</span><span class="sxs-lookup"><span data-stu-id="74a21-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="74a21-112">取得指定非邊緣裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="74a21-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="74a21-113">參數</span><span class="sxs-lookup"><span data-stu-id="74a21-113">PARAMETERS</span></span>

### <span data-ttu-id="74a21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a21-114">-DefaultProfile</span></span>
<span data-ttu-id="74a21-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74a21-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a21-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="74a21-116">-DeviceId</span></span>
<span data-ttu-id="74a21-117">非邊緣裝置的 Id。</span><span class="sxs-lookup"><span data-stu-id="74a21-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="74a21-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74a21-118">-InputObject</span></span>
<span data-ttu-id="74a21-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="74a21-119">IotHub object</span></span>

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

### <span data-ttu-id="74a21-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="74a21-120">-IotHubName</span></span>
<span data-ttu-id="74a21-121">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="74a21-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="74a21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a21-122">-ResourceGroupName</span></span>
<span data-ttu-id="74a21-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="74a21-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="74a21-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74a21-124">-ResourceId</span></span>
<span data-ttu-id="74a21-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="74a21-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="74a21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a21-126">CommonParameters</span></span>
<span data-ttu-id="74a21-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74a21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a21-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74a21-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a21-129">輸入</span><span class="sxs-lookup"><span data-stu-id="74a21-129">INPUTS</span></span>

### <span data-ttu-id="74a21-130">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="74a21-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="74a21-131">System.object</span><span class="sxs-lookup"><span data-stu-id="74a21-131">System.String</span></span>

## <span data-ttu-id="74a21-132">輸出</span><span class="sxs-lookup"><span data-stu-id="74a21-132">OUTPUTS</span></span>

### <span data-ttu-id="74a21-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="74a21-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="74a21-134">筆記</span><span class="sxs-lookup"><span data-stu-id="74a21-134">NOTES</span></span>

## <span data-ttu-id="74a21-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="74a21-135">RELATED LINKS</span></span>