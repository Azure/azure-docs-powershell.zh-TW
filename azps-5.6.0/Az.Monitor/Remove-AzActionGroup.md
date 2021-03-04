---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 50d9e49319f8171ea8c0fea93e9474bd175b417f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906909"
---
# <span data-ttu-id="d90bf-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="d90bf-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="d90bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d90bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d90bf-103">移除動作群組。</span><span class="sxs-lookup"><span data-stu-id="d90bf-103">Removes an action group.</span></span>

## <span data-ttu-id="d90bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="d90bf-104">SYNTAX</span></span>

### <span data-ttu-id="d90bf-105">ByPropertyName (預設) </span><span class="sxs-lookup"><span data-stu-id="d90bf-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d90bf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d90bf-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d90bf-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d90bf-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d90bf-108">描述</span><span class="sxs-lookup"><span data-stu-id="d90bf-108">DESCRIPTION</span></span>
<span data-ttu-id="d90bf-109">**Remove-AzActionGroup** Cmdlet 會移除動作群組。</span><span class="sxs-lookup"><span data-stu-id="d90bf-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="d90bf-110">例子</span><span class="sxs-lookup"><span data-stu-id="d90bf-110">EXAMPLES</span></span>

### <span data-ttu-id="d90bf-111">範例 1：移除動作群組</span><span class="sxs-lookup"><span data-stu-id="d90bf-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="d90bf-112">參數</span><span class="sxs-lookup"><span data-stu-id="d90bf-112">PARAMETERS</span></span>

### <span data-ttu-id="d90bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90bf-113">-DefaultProfile</span></span>
<span data-ttu-id="d90bf-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d90bf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d90bf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d90bf-115">-InputObject</span></span>
<span data-ttu-id="d90bf-116">動作群組資源</span><span class="sxs-lookup"><span data-stu-id="d90bf-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d90bf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d90bf-117">-Name</span></span>
<span data-ttu-id="d90bf-118">動作組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d90bf-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d90bf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90bf-119">-ResourceGroupName</span></span>
<span data-ttu-id="d90bf-120">資源群組的命名</span><span class="sxs-lookup"><span data-stu-id="d90bf-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d90bf-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d90bf-121">-ResourceId</span></span>
<span data-ttu-id="d90bf-122">資源 i</span><span class="sxs-lookup"><span data-stu-id="d90bf-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d90bf-123">-確認</span><span class="sxs-lookup"><span data-stu-id="d90bf-123">-Confirm</span></span>
<span data-ttu-id="d90bf-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d90bf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90bf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90bf-125">-WhatIf</span></span>
<span data-ttu-id="d90bf-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d90bf-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d90bf-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d90bf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90bf-128">CommonParameters</span></span>
<span data-ttu-id="d90bf-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d90bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90bf-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d90bf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90bf-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d90bf-131">INPUTS</span></span>

### <span data-ttu-id="d90bf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d90bf-132">System.String</span></span>

### <span data-ttu-id="d90bf-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="d90bf-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="d90bf-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d90bf-134">OUTPUTS</span></span>

### <span data-ttu-id="d90bf-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d90bf-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d90bf-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d90bf-136">NOTES</span></span>

## <span data-ttu-id="d90bf-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d90bf-137">RELATED LINKS</span></span>

<span data-ttu-id="d90bf-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
[Get-AzActionGroup](./Get-AzActionGroup.md) 
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="d90bf-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
