---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: fe3d020bb32e120fe103dd8f90bfbb1d83d9a21d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795233"
---
# <span data-ttu-id="579cb-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="579cb-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="579cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="579cb-102">SYNOPSIS</span></span>
<span data-ttu-id="579cb-103">從管理群組中移除訂閱。</span><span class="sxs-lookup"><span data-stu-id="579cb-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="579cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="579cb-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="579cb-105">說明</span><span class="sxs-lookup"><span data-stu-id="579cb-105">DESCRIPTION</span></span>
<span data-ttu-id="579cb-106">**AzManagementGroupSubscription** Cmdlet 會從管理群組中移除訂閱。</span><span class="sxs-lookup"><span data-stu-id="579cb-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="579cb-107">示例</span><span class="sxs-lookup"><span data-stu-id="579cb-107">EXAMPLES</span></span>

### <span data-ttu-id="579cb-108">範例 1-從管理群組中移除訂閱</span><span class="sxs-lookup"><span data-stu-id="579cb-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="579cb-109">參數</span><span class="sxs-lookup"><span data-stu-id="579cb-109">PARAMETERS</span></span>

### <span data-ttu-id="579cb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579cb-110">-DefaultProfile</span></span>
<span data-ttu-id="579cb-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="579cb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579cb-112">-[名]</span><span class="sxs-lookup"><span data-stu-id="579cb-112">-GroupName</span></span>
<span data-ttu-id="579cb-113">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="579cb-113">Management Group Id</span></span>

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

### <span data-ttu-id="579cb-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="579cb-114">-PassThru</span></span>
<span data-ttu-id="579cb-115">`true`成功執行後返回</span><span class="sxs-lookup"><span data-stu-id="579cb-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="579cb-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="579cb-116">-SubscriptionId</span></span>
<span data-ttu-id="579cb-117">Witht 管理相關聯之訂閱的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="579cb-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="579cb-118">-確認</span><span class="sxs-lookup"><span data-stu-id="579cb-118">-Confirm</span></span>
<span data-ttu-id="579cb-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="579cb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="579cb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="579cb-120">-WhatIf</span></span>
<span data-ttu-id="579cb-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="579cb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="579cb-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="579cb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="579cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579cb-123">CommonParameters</span></span>
<span data-ttu-id="579cb-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="579cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579cb-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="579cb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579cb-126">輸入</span><span class="sxs-lookup"><span data-stu-id="579cb-126">INPUTS</span></span>

### <span data-ttu-id="579cb-127">所有</span><span class="sxs-lookup"><span data-stu-id="579cb-127">None</span></span>

## <span data-ttu-id="579cb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="579cb-128">OUTPUTS</span></span>

### <span data-ttu-id="579cb-129">System.object</span><span class="sxs-lookup"><span data-stu-id="579cb-129">System.Boolean</span></span>

## <span data-ttu-id="579cb-130">筆記</span><span class="sxs-lookup"><span data-stu-id="579cb-130">NOTES</span></span>

## <span data-ttu-id="579cb-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="579cb-131">RELATED LINKS</span></span>
