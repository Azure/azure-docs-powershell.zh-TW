---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129158"
---
# <span data-ttu-id="4c3fd-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4c3fd-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="4c3fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3fd-103">更新 Microsoft 合作夥伴網路 (MPN 目前已驗證的使用者或服務主體) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="4c3fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c3fd-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c3fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="4c3fd-106">更新 Microsoft 合作夥伴網路 (MPN 目前已驗證的使用者或服務主體) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="4c3fd-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c3fd-107">EXAMPLES</span></span>

### <span data-ttu-id="4c3fd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4c3fd-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="4c3fd-109">將管理合作夥伴更新為新的管理夥伴</span><span class="sxs-lookup"><span data-stu-id="4c3fd-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="4c3fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c3fd-110">PARAMETERS</span></span>

### <span data-ttu-id="4c3fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3fd-111">-DefaultProfile</span></span>
<span data-ttu-id="4c3fd-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c3fd-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="4c3fd-113">-PartnerId</span></span>
<span data-ttu-id="4c3fd-114">管理合作夥伴識別碼，它是6位數的數位</span><span class="sxs-lookup"><span data-stu-id="4c3fd-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="4c3fd-115">-確認</span><span class="sxs-lookup"><span data-stu-id="4c3fd-115">-Confirm</span></span>
<span data-ttu-id="4c3fd-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c3fd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c3fd-117">-WhatIf</span></span>
<span data-ttu-id="4c3fd-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c3fd-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c3fd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3fd-120">CommonParameters</span></span>
<span data-ttu-id="4c3fd-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3fd-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c3fd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3fd-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4c3fd-123">INPUTS</span></span>

### <span data-ttu-id="4c3fd-124">所有</span><span class="sxs-lookup"><span data-stu-id="4c3fd-124">None</span></span>

## <span data-ttu-id="4c3fd-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4c3fd-125">OUTPUTS</span></span>

### <span data-ttu-id="4c3fd-126">PSManagementPartner 中的 ManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4c3fd-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="4c3fd-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4c3fd-127">NOTES</span></span>

## <span data-ttu-id="4c3fd-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c3fd-128">RELATED LINKS</span></span>

[<span data-ttu-id="4c3fd-129">移除-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4c3fd-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="4c3fd-130">新-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4c3fd-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="4c3fd-131">AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4c3fd-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)