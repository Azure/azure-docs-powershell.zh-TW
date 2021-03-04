---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: af4b605c25ff3c35b0235612d7258be66a772c43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902881"
---
# <span data-ttu-id="e0934-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="e0934-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="e0934-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e0934-102">SYNOPSIS</span></span>
<span data-ttu-id="e0934-103">設定指定裝置之父裝置。</span><span class="sxs-lookup"><span data-stu-id="e0934-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="e0934-104">語法</span><span class="sxs-lookup"><span data-stu-id="e0934-104">SYNTAX</span></span>

### <span data-ttu-id="e0934-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e0934-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0934-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e0934-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0934-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e0934-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0934-108">描述</span><span class="sxs-lookup"><span data-stu-id="e0934-108">DESCRIPTION</span></span>
<span data-ttu-id="e0934-109">設定指定非邊緣裝置之父裝置。</span><span class="sxs-lookup"><span data-stu-id="e0934-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="e0934-110">例子</span><span class="sxs-lookup"><span data-stu-id="e0934-110">EXAMPLES</span></span>

### <span data-ttu-id="e0934-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e0934-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
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
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="e0934-112">參數</span><span class="sxs-lookup"><span data-stu-id="e0934-112">PARAMETERS</span></span>

### <span data-ttu-id="e0934-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0934-113">-DefaultProfile</span></span>
<span data-ttu-id="e0934-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0934-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0934-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e0934-115">-DeviceId</span></span>
<span data-ttu-id="e0934-116">非邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0934-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="e0934-117">-強制</span><span class="sxs-lookup"><span data-stu-id="e0934-117">-Force</span></span>
<span data-ttu-id="e0934-118">覆寫非邊緣裝置父裝置。</span><span class="sxs-lookup"><span data-stu-id="e0934-118">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0934-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0934-119">-InputObject</span></span>
<span data-ttu-id="e0934-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="e0934-120">IotHub object</span></span>

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

### <span data-ttu-id="e0934-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e0934-121">-IotHubName</span></span>
<span data-ttu-id="e0934-122">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="e0934-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e0934-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="e0934-123">-ParentDeviceId</span></span>
<span data-ttu-id="e0934-124">邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0934-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0934-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0934-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0934-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="e0934-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e0934-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0934-127">-ResourceId</span></span>
<span data-ttu-id="e0934-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e0934-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e0934-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e0934-129">-Confirm</span></span>
<span data-ttu-id="e0934-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e0934-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0934-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0934-131">-WhatIf</span></span>
<span data-ttu-id="e0934-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0934-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0934-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0934-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0934-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0934-134">CommonParameters</span></span>
<span data-ttu-id="e0934-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e0934-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0934-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e0934-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0934-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e0934-137">INPUTS</span></span>

### <span data-ttu-id="e0934-138">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e0934-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e0934-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e0934-139">System.String</span></span>

## <span data-ttu-id="e0934-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e0934-140">OUTPUTS</span></span>

### <span data-ttu-id="e0934-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="e0934-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="e0934-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e0934-142">NOTES</span></span>

## <span data-ttu-id="e0934-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0934-143">RELATED LINKS</span></span>
