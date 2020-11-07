---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: a3ef84ef6740eb0d505ff2f9f69670ea83242deb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798301"
---
# <span data-ttu-id="e415d-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="e415d-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="e415d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e415d-102">SYNOPSIS</span></span>
<span data-ttu-id="e415d-103">新增訂閱給管理群組。</span><span class="sxs-lookup"><span data-stu-id="e415d-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="e415d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e415d-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e415d-105">說明</span><span class="sxs-lookup"><span data-stu-id="e415d-105">DESCRIPTION</span></span>
<span data-ttu-id="e415d-106">**AzManagementGroupSubscription** Cmdlet 會新增訂閱給管理群組。</span><span class="sxs-lookup"><span data-stu-id="e415d-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="e415d-107">示例</span><span class="sxs-lookup"><span data-stu-id="e415d-107">EXAMPLES</span></span>

### <span data-ttu-id="e415d-108">範例1：新增訂閱至管理群組</span><span class="sxs-lookup"><span data-stu-id="e415d-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="e415d-109">參數</span><span class="sxs-lookup"><span data-stu-id="e415d-109">PARAMETERS</span></span>

### <span data-ttu-id="e415d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e415d-110">-DefaultProfile</span></span>
<span data-ttu-id="e415d-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e415d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e415d-112">-[名]</span><span class="sxs-lookup"><span data-stu-id="e415d-112">-GroupName</span></span>
<span data-ttu-id="e415d-113">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="e415d-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e415d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e415d-114">-PassThru</span></span>
<span data-ttu-id="e415d-115">`true`成功執行後返回</span><span class="sxs-lookup"><span data-stu-id="e415d-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="e415d-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e415d-116">-SubscriptionId</span></span>
<span data-ttu-id="e415d-117">與管理相關聯之訂閱的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="e415d-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="e415d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="e415d-118">-Confirm</span></span>
<span data-ttu-id="e415d-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e415d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e415d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e415d-120">-WhatIf</span></span>
<span data-ttu-id="e415d-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e415d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e415d-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e415d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e415d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e415d-123">CommonParameters</span></span>
<span data-ttu-id="e415d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e415d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e415d-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e415d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e415d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e415d-126">INPUTS</span></span>

### <span data-ttu-id="e415d-127">所有</span><span class="sxs-lookup"><span data-stu-id="e415d-127">None</span></span>

## <span data-ttu-id="e415d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e415d-128">OUTPUTS</span></span>

### <span data-ttu-id="e415d-129">System.object</span><span class="sxs-lookup"><span data-stu-id="e415d-129">System.Boolean</span></span>

## <span data-ttu-id="e415d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e415d-130">NOTES</span></span>

## <span data-ttu-id="e415d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e415d-131">RELATED LINKS</span></span>
