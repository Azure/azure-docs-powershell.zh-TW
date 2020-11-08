---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971399"
---
# <span data-ttu-id="0a321-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0a321-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="0a321-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a321-102">SYNOPSIS</span></span>
<span data-ttu-id="0a321-103">將 Microsoft Partner Network (MPN) 識別碼與目前已驗證身份的使用者或服務主體相關聯。</span><span class="sxs-lookup"><span data-stu-id="0a321-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0a321-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a321-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a321-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a321-105">DESCRIPTION</span></span>
<span data-ttu-id="0a321-106">將 Microsoft Partner Network (MPN) 識別碼與目前已驗證身份的使用者或服務主體相關聯。</span><span class="sxs-lookup"><span data-stu-id="0a321-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0a321-107">示例</span><span class="sxs-lookup"><span data-stu-id="0a321-107">EXAMPLES</span></span>

### <span data-ttu-id="0a321-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0a321-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0a321-109">新增管理合作夥伴</span><span class="sxs-lookup"><span data-stu-id="0a321-109">Add a management partner</span></span>

## <span data-ttu-id="0a321-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a321-110">PARAMETERS</span></span>

### <span data-ttu-id="0a321-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a321-111">-DefaultProfile</span></span>
<span data-ttu-id="0a321-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a321-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a321-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0a321-113">-PartnerId</span></span>
<span data-ttu-id="0a321-114">管理合作夥伴識別碼，它是6位數的數位</span><span class="sxs-lookup"><span data-stu-id="0a321-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="0a321-115">-確認</span><span class="sxs-lookup"><span data-stu-id="0a321-115">-Confirm</span></span>
<span data-ttu-id="0a321-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a321-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a321-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a321-117">-WhatIf</span></span>
<span data-ttu-id="0a321-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a321-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a321-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a321-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a321-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a321-120">CommonParameters</span></span>
<span data-ttu-id="0a321-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a321-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a321-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a321-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a321-123">輸入</span><span class="sxs-lookup"><span data-stu-id="0a321-123">INPUTS</span></span>

### <span data-ttu-id="0a321-124">所有</span><span class="sxs-lookup"><span data-stu-id="0a321-124">None</span></span>

## <span data-ttu-id="0a321-125">輸出</span><span class="sxs-lookup"><span data-stu-id="0a321-125">OUTPUTS</span></span>

### <span data-ttu-id="0a321-126">PSManagementPartner 中的 ManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0a321-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="0a321-127">筆記</span><span class="sxs-lookup"><span data-stu-id="0a321-127">NOTES</span></span>

## <span data-ttu-id="0a321-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a321-128">RELATED LINKS</span></span>

[<span data-ttu-id="0a321-129">移除-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0a321-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="0a321-130">AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0a321-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="0a321-131">更新-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0a321-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)