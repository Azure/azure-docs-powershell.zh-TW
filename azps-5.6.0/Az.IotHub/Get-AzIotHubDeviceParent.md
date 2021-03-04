---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 06eb84ea854e9c0262f6f3e00e3e13e90f630baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911069"
---
# <span data-ttu-id="7eaba-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="7eaba-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="7eaba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7eaba-102">SYNOPSIS</span></span>
<span data-ttu-id="7eaba-103">取得指定裝置中的父裝置。</span><span class="sxs-lookup"><span data-stu-id="7eaba-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="7eaba-104">語法</span><span class="sxs-lookup"><span data-stu-id="7eaba-104">SYNTAX</span></span>

### <span data-ttu-id="7eaba-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7eaba-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eaba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7eaba-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eaba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7eaba-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eaba-108">描述</span><span class="sxs-lookup"><span data-stu-id="7eaba-108">DESCRIPTION</span></span>
<span data-ttu-id="7eaba-109">取得指定的非邊緣裝置之父裝置。</span><span class="sxs-lookup"><span data-stu-id="7eaba-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="7eaba-110">例子</span><span class="sxs-lookup"><span data-stu-id="7eaba-110">EXAMPLES</span></span>

### <span data-ttu-id="7eaba-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7eaba-111">Example 1</span></span>
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

<span data-ttu-id="7eaba-112">取得指定的非邊緣裝置之父裝置。</span><span class="sxs-lookup"><span data-stu-id="7eaba-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="7eaba-113">參數</span><span class="sxs-lookup"><span data-stu-id="7eaba-113">PARAMETERS</span></span>

### <span data-ttu-id="7eaba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eaba-114">-DefaultProfile</span></span>
<span data-ttu-id="7eaba-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7eaba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eaba-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7eaba-116">-DeviceId</span></span>
<span data-ttu-id="7eaba-117">非邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7eaba-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="7eaba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eaba-118">-InputObject</span></span>
<span data-ttu-id="7eaba-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="7eaba-119">IotHub object</span></span>

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

### <span data-ttu-id="7eaba-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7eaba-120">-IotHubName</span></span>
<span data-ttu-id="7eaba-121">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="7eaba-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7eaba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eaba-122">-ResourceGroupName</span></span>
<span data-ttu-id="7eaba-123">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="7eaba-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7eaba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eaba-124">-ResourceId</span></span>
<span data-ttu-id="7eaba-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7eaba-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7eaba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eaba-126">CommonParameters</span></span>
<span data-ttu-id="7eaba-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7eaba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eaba-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7eaba-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eaba-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7eaba-129">INPUTS</span></span>

### <span data-ttu-id="7eaba-130">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7eaba-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7eaba-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7eaba-131">System.String</span></span>

## <span data-ttu-id="7eaba-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7eaba-132">OUTPUTS</span></span>

### <span data-ttu-id="7eaba-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="7eaba-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="7eaba-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7eaba-134">NOTES</span></span>

## <span data-ttu-id="7eaba-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eaba-135">RELATED LINKS</span></span>
