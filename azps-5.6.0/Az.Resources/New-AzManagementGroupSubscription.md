---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: ecd5771478f3d3ff3cee4a5045d6c72eb707af11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912317"
---
# <span data-ttu-id="9ca66-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="9ca66-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="9ca66-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9ca66-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca66-103">新增訂閱至管理群組。</span><span class="sxs-lookup"><span data-stu-id="9ca66-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="9ca66-104">語法</span><span class="sxs-lookup"><span data-stu-id="9ca66-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca66-105">描述</span><span class="sxs-lookup"><span data-stu-id="9ca66-105">DESCRIPTION</span></span>
<span data-ttu-id="9ca66-106">**New-AzManagementGroupSubscription** Cmdlet 會將訂閱新增到管理群組。</span><span class="sxs-lookup"><span data-stu-id="9ca66-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="9ca66-107">例子</span><span class="sxs-lookup"><span data-stu-id="9ca66-107">EXAMPLES</span></span>

### <span data-ttu-id="9ca66-108">範例 1：新增訂閱至管理群組</span><span class="sxs-lookup"><span data-stu-id="9ca66-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="9ca66-109">參數</span><span class="sxs-lookup"><span data-stu-id="9ca66-109">PARAMETERS</span></span>

### <span data-ttu-id="9ca66-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca66-110">-DefaultProfile</span></span>
<span data-ttu-id="9ca66-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ca66-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca66-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="9ca66-112">-GroupName</span></span>
<span data-ttu-id="9ca66-113">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="9ca66-113">Management Group Id</span></span>

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

### <span data-ttu-id="9ca66-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ca66-114">-PassThru</span></span>
<span data-ttu-id="9ca66-115">成功 `true` 執行時返回</span><span class="sxs-lookup"><span data-stu-id="9ca66-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="9ca66-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ca66-116">-SubscriptionId</span></span>
<span data-ttu-id="9ca66-117">與管理相關聯的訂閱的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="9ca66-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="9ca66-118">-確認</span><span class="sxs-lookup"><span data-stu-id="9ca66-118">-Confirm</span></span>
<span data-ttu-id="9ca66-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9ca66-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca66-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca66-120">-WhatIf</span></span>
<span data-ttu-id="9ca66-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ca66-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ca66-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ca66-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca66-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca66-123">CommonParameters</span></span>
<span data-ttu-id="9ca66-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9ca66-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca66-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ca66-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca66-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9ca66-126">INPUTS</span></span>

### <span data-ttu-id="9ca66-127">沒有</span><span class="sxs-lookup"><span data-stu-id="9ca66-127">None</span></span>

## <span data-ttu-id="9ca66-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9ca66-128">OUTPUTS</span></span>

### <span data-ttu-id="9ca66-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ca66-129">System.Boolean</span></span>

## <span data-ttu-id="9ca66-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9ca66-130">NOTES</span></span>

## <span data-ttu-id="9ca66-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ca66-131">RELATED LINKS</span></span>
