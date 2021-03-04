---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 30d13f9a5f9338a33f8ec6f6aaba9b40e028f087
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905837"
---
# <span data-ttu-id="f738d-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f738d-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="f738d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f738d-102">SYNOPSIS</span></span>
<span data-ttu-id="f738d-103">從管理群組移除訂閱。</span><span class="sxs-lookup"><span data-stu-id="f738d-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f738d-104">語法</span><span class="sxs-lookup"><span data-stu-id="f738d-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f738d-105">描述</span><span class="sxs-lookup"><span data-stu-id="f738d-105">DESCRIPTION</span></span>
<span data-ttu-id="f738d-106">**Remove-AzManagementGroupSubscription** Cmdlet 會從管理群組移除訂閱。</span><span class="sxs-lookup"><span data-stu-id="f738d-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f738d-107">例子</span><span class="sxs-lookup"><span data-stu-id="f738d-107">EXAMPLES</span></span>

### <span data-ttu-id="f738d-108">範例 1：從管理群組移除訂閱</span><span class="sxs-lookup"><span data-stu-id="f738d-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f738d-109">參數</span><span class="sxs-lookup"><span data-stu-id="f738d-109">PARAMETERS</span></span>

### <span data-ttu-id="f738d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f738d-110">-DefaultProfile</span></span>
<span data-ttu-id="f738d-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f738d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f738d-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f738d-112">-GroupName</span></span>
<span data-ttu-id="f738d-113">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="f738d-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f738d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f738d-114">-PassThru</span></span>
<span data-ttu-id="f738d-115">成功 `true` 執行時返回</span><span class="sxs-lookup"><span data-stu-id="f738d-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f738d-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f738d-116">-SubscriptionId</span></span>
<span data-ttu-id="f738d-117">與管理相關聯的訂閱的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="f738d-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f738d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f738d-118">-Confirm</span></span>
<span data-ttu-id="f738d-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f738d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f738d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f738d-120">-WhatIf</span></span>
<span data-ttu-id="f738d-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f738d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f738d-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f738d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f738d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f738d-123">CommonParameters</span></span>
<span data-ttu-id="f738d-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f738d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f738d-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f738d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f738d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f738d-126">INPUTS</span></span>

### <span data-ttu-id="f738d-127">沒有</span><span class="sxs-lookup"><span data-stu-id="f738d-127">None</span></span>

## <span data-ttu-id="f738d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f738d-128">OUTPUTS</span></span>

### <span data-ttu-id="f738d-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f738d-129">System.Boolean</span></span>

## <span data-ttu-id="f738d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f738d-130">NOTES</span></span>

## <span data-ttu-id="f738d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f738d-131">RELATED LINKS</span></span>
