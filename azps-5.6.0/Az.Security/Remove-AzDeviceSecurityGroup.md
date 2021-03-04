---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: 302e4b096c3a41c6dd5a57a87d23bf15b83c96a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909957"
---
# <span data-ttu-id="f4958-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f4958-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="f4958-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f4958-102">SYNOPSIS</span></span>
<span data-ttu-id="f4958-103">刪除裝置安全性群組</span><span class="sxs-lookup"><span data-stu-id="f4958-103">Delete device security group</span></span>

## <span data-ttu-id="f4958-104">語法</span><span class="sxs-lookup"><span data-stu-id="f4958-104">SYNTAX</span></span>

### <span data-ttu-id="f4958-105">ResourceIdLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f4958-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4958-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4958-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4958-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4958-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4958-108">描述</span><span class="sxs-lookup"><span data-stu-id="f4958-108">DESCRIPTION</span></span>
<span data-ttu-id="f4958-109">Cmdlet Remove-AzDeviceSecurityGroup刪除 iot 安全性解決方案中定義的裝置安全性群組。</span><span class="sxs-lookup"><span data-stu-id="f4958-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="f4958-110">例子</span><span class="sxs-lookup"><span data-stu-id="f4958-110">EXAMPLES</span></span>

### <span data-ttu-id="f4958-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f4958-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="f4958-112">刪除具有資源識別碼 "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 的 iot Hub 中樞裝置安全性群組 "MySecurityGroup"</span><span class="sxs-lookup"><span data-stu-id="f4958-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="f4958-113">參數</span><span class="sxs-lookup"><span data-stu-id="f4958-113">PARAMETERS</span></span>

### <span data-ttu-id="f4958-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4958-114">-DefaultProfile</span></span>
<span data-ttu-id="f4958-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4958-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4958-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="f4958-116">-HubResourceId</span></span>
<span data-ttu-id="f4958-117">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4958-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4958-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4958-118">-InputObject</span></span>
<span data-ttu-id="f4958-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="f4958-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4958-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4958-120">-Name</span></span>
<span data-ttu-id="f4958-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f4958-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4958-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4958-122">-PassThru</span></span>
<span data-ttu-id="f4958-123">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="f4958-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f4958-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4958-124">-ResourceId</span></span>
<span data-ttu-id="f4958-125">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4958-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4958-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f4958-126">-Confirm</span></span>
<span data-ttu-id="f4958-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f4958-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4958-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4958-128">-WhatIf</span></span>
<span data-ttu-id="f4958-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4958-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4958-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4958-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4958-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4958-131">CommonParameters</span></span>
<span data-ttu-id="f4958-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f4958-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4958-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4958-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4958-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f4958-134">INPUTS</span></span>

### <span data-ttu-id="f4958-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f4958-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="f4958-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f4958-136">System.String</span></span>

## <span data-ttu-id="f4958-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f4958-137">OUTPUTS</span></span>

### <span data-ttu-id="f4958-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4958-138">System.Boolean</span></span>

## <span data-ttu-id="f4958-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f4958-139">NOTES</span></span>

## <span data-ttu-id="f4958-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4958-140">RELATED LINKS</span></span>
