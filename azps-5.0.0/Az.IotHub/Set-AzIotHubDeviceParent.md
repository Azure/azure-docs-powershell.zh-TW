---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141694"
---
# <span data-ttu-id="92f3c-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="92f3c-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="92f3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="92f3c-103">設定指定裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="92f3c-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="92f3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="92f3c-104">SYNTAX</span></span>

### <span data-ttu-id="92f3c-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="92f3c-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92f3c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92f3c-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92f3c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="92f3c-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92f3c-108">說明</span><span class="sxs-lookup"><span data-stu-id="92f3c-108">DESCRIPTION</span></span>
<span data-ttu-id="92f3c-109">設定指定非邊緣裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="92f3c-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="92f3c-110">示例</span><span class="sxs-lookup"><span data-stu-id="92f3c-110">EXAMPLES</span></span>

### <span data-ttu-id="92f3c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="92f3c-111">Example 1</span></span>
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

## <span data-ttu-id="92f3c-112">參數</span><span class="sxs-lookup"><span data-stu-id="92f3c-112">PARAMETERS</span></span>

### <span data-ttu-id="92f3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f3c-113">-DefaultProfile</span></span>
<span data-ttu-id="92f3c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92f3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f3c-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="92f3c-115">-DeviceId</span></span>
<span data-ttu-id="92f3c-116">非邊緣裝置的 Id。</span><span class="sxs-lookup"><span data-stu-id="92f3c-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="92f3c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="92f3c-117">-Force</span></span>
<span data-ttu-id="92f3c-118">覆寫非邊緣裝置的父裝置。</span><span class="sxs-lookup"><span data-stu-id="92f3c-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="92f3c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92f3c-119">-InputObject</span></span>
<span data-ttu-id="92f3c-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="92f3c-120">IotHub object</span></span>

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

### <span data-ttu-id="92f3c-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="92f3c-121">-IotHubName</span></span>
<span data-ttu-id="92f3c-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="92f3c-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="92f3c-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="92f3c-123">-ParentDeviceId</span></span>
<span data-ttu-id="92f3c-124">Edge 裝置的 Id。</span><span class="sxs-lookup"><span data-stu-id="92f3c-124">Id of edge device.</span></span>

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

### <span data-ttu-id="92f3c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f3c-125">-ResourceGroupName</span></span>
<span data-ttu-id="92f3c-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="92f3c-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="92f3c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92f3c-127">-ResourceId</span></span>
<span data-ttu-id="92f3c-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="92f3c-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="92f3c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="92f3c-129">-Confirm</span></span>
<span data-ttu-id="92f3c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92f3c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92f3c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92f3c-131">-WhatIf</span></span>
<span data-ttu-id="92f3c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92f3c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92f3c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92f3c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92f3c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f3c-134">CommonParameters</span></span>
<span data-ttu-id="92f3c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92f3c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f3c-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92f3c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f3c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="92f3c-137">INPUTS</span></span>

### <span data-ttu-id="92f3c-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="92f3c-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="92f3c-139">System.object</span><span class="sxs-lookup"><span data-stu-id="92f3c-139">System.String</span></span>

## <span data-ttu-id="92f3c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="92f3c-140">OUTPUTS</span></span>

### <span data-ttu-id="92f3c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="92f3c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="92f3c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="92f3c-142">NOTES</span></span>

## <span data-ttu-id="92f3c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="92f3c-143">RELATED LINKS</span></span>
