---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277664"
---
# <span data-ttu-id="b7448-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7448-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="b7448-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7448-102">SYNOPSIS</span></span>
<span data-ttu-id="b7448-103">刪除裝置安全性群組</span><span class="sxs-lookup"><span data-stu-id="b7448-103">Delete device security group</span></span>

## <span data-ttu-id="b7448-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7448-104">SYNTAX</span></span>

### <span data-ttu-id="b7448-105">ResourceIdLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b7448-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7448-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7448-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7448-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7448-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7448-108">說明</span><span class="sxs-lookup"><span data-stu-id="b7448-108">DESCRIPTION</span></span>
<span data-ttu-id="b7448-109">Remove-AzDeviceSecurityGroup Cmdlet 會刪除在 iot 安全解決方案中定義的裝置安全性群組。</span><span class="sxs-lookup"><span data-stu-id="b7448-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="b7448-110">示例</span><span class="sxs-lookup"><span data-stu-id="b7448-110">EXAMPLES</span></span>

### <span data-ttu-id="b7448-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b7448-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="b7448-112">刪除 iot 中樞的裝置安全性群組 "MySecurityGroup" 與資源 id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="b7448-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="b7448-113">參數</span><span class="sxs-lookup"><span data-stu-id="b7448-113">PARAMETERS</span></span>

### <span data-ttu-id="b7448-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7448-114">-DefaultProfile</span></span>
<span data-ttu-id="b7448-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7448-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7448-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="b7448-116">-HubResourceId</span></span>
<span data-ttu-id="b7448-117">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7448-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b7448-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7448-118">-InputObject</span></span>
<span data-ttu-id="b7448-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="b7448-119">Input Object.</span></span>

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

### <span data-ttu-id="b7448-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7448-120">-Name</span></span>
<span data-ttu-id="b7448-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b7448-121">Resource name.</span></span>

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

### <span data-ttu-id="b7448-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7448-122">-PassThru</span></span>
<span data-ttu-id="b7448-123">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="b7448-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b7448-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7448-124">-ResourceId</span></span>
<span data-ttu-id="b7448-125">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7448-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b7448-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b7448-126">-Confirm</span></span>
<span data-ttu-id="b7448-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7448-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7448-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7448-128">-WhatIf</span></span>
<span data-ttu-id="b7448-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7448-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7448-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7448-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7448-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7448-131">CommonParameters</span></span>
<span data-ttu-id="b7448-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7448-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7448-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b7448-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7448-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b7448-134">INPUTS</span></span>

### <span data-ttu-id="b7448-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7448-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="b7448-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b7448-136">System.String</span></span>

## <span data-ttu-id="b7448-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b7448-137">OUTPUTS</span></span>

### <span data-ttu-id="b7448-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b7448-138">System.Boolean</span></span>

## <span data-ttu-id="b7448-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b7448-139">NOTES</span></span>

## <span data-ttu-id="b7448-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7448-140">RELATED LINKS</span></span>
