---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 57d9f5d51cb2646274728f8b2f6d846bd954f2a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912829"
---
# <span data-ttu-id="73162-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73162-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="73162-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73162-102">SYNOPSIS</span></span>
<span data-ttu-id="73162-103">將 Microsoft 合作夥伴網路 (MPN) 識別碼與目前驗證的使用者或服務主體建立關聯。</span><span class="sxs-lookup"><span data-stu-id="73162-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="73162-104">語法</span><span class="sxs-lookup"><span data-stu-id="73162-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73162-105">描述</span><span class="sxs-lookup"><span data-stu-id="73162-105">DESCRIPTION</span></span>
<span data-ttu-id="73162-106">將 Microsoft 合作夥伴網路 (MPN) 識別碼與目前驗證的使用者或服務主體建立關聯。</span><span class="sxs-lookup"><span data-stu-id="73162-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="73162-107">例子</span><span class="sxs-lookup"><span data-stu-id="73162-107">EXAMPLES</span></span>

### <span data-ttu-id="73162-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="73162-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="73162-109">新增管理合作夥伴</span><span class="sxs-lookup"><span data-stu-id="73162-109">Add a management partner</span></span>

## <span data-ttu-id="73162-110">參數</span><span class="sxs-lookup"><span data-stu-id="73162-110">PARAMETERS</span></span>

### <span data-ttu-id="73162-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73162-111">-DefaultProfile</span></span>
<span data-ttu-id="73162-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="73162-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73162-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="73162-113">-PartnerId</span></span>
<span data-ttu-id="73162-114">管理合作夥伴識別碼，為 6 位數號碼</span><span class="sxs-lookup"><span data-stu-id="73162-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="73162-115">-確認</span><span class="sxs-lookup"><span data-stu-id="73162-115">-Confirm</span></span>
<span data-ttu-id="73162-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="73162-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73162-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73162-117">-WhatIf</span></span>
<span data-ttu-id="73162-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73162-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73162-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73162-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73162-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73162-120">CommonParameters</span></span>
<span data-ttu-id="73162-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73162-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73162-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="73162-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73162-123">輸入</span><span class="sxs-lookup"><span data-stu-id="73162-123">INPUTS</span></span>

### <span data-ttu-id="73162-124">沒有</span><span class="sxs-lookup"><span data-stu-id="73162-124">None</span></span>

## <span data-ttu-id="73162-125">輸出</span><span class="sxs-lookup"><span data-stu-id="73162-125">OUTPUTS</span></span>

### <span data-ttu-id="73162-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73162-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="73162-127">筆記</span><span class="sxs-lookup"><span data-stu-id="73162-127">NOTES</span></span>

## <span data-ttu-id="73162-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="73162-128">RELATED LINKS</span></span>

[<span data-ttu-id="73162-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73162-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="73162-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73162-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="73162-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73162-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)