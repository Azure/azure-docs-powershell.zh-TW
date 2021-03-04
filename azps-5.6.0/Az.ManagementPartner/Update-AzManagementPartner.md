---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 493f4b3e1cfaa3be59d0bd402e2c0d13dfdfad4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916126"
---
# <span data-ttu-id="712f2-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="712f2-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="712f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="712f2-102">SYNOPSIS</span></span>
<span data-ttu-id="712f2-103">更新 Microsoft 合作夥伴網路 (MPN) 驗證之使用者或服務主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="712f2-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="712f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="712f2-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="712f2-105">描述</span><span class="sxs-lookup"><span data-stu-id="712f2-105">DESCRIPTION</span></span>
<span data-ttu-id="712f2-106">更新 Microsoft 合作夥伴網路 (MPN) 驗證之使用者或服務主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="712f2-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="712f2-107">例子</span><span class="sxs-lookup"><span data-stu-id="712f2-107">EXAMPLES</span></span>

### <span data-ttu-id="712f2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="712f2-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="712f2-109">將管理合作夥伴更新至新合作夥伴</span><span class="sxs-lookup"><span data-stu-id="712f2-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="712f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="712f2-110">PARAMETERS</span></span>

### <span data-ttu-id="712f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712f2-111">-DefaultProfile</span></span>
<span data-ttu-id="712f2-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="712f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="712f2-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="712f2-113">-PartnerId</span></span>
<span data-ttu-id="712f2-114">管理合作夥伴識別碼，這是 6 位數的數位</span><span class="sxs-lookup"><span data-stu-id="712f2-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="712f2-115">-確認</span><span class="sxs-lookup"><span data-stu-id="712f2-115">-Confirm</span></span>
<span data-ttu-id="712f2-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="712f2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="712f2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="712f2-117">-WhatIf</span></span>
<span data-ttu-id="712f2-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="712f2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="712f2-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="712f2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="712f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712f2-120">CommonParameters</span></span>
<span data-ttu-id="712f2-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="712f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712f2-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="712f2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712f2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="712f2-123">INPUTS</span></span>

### <span data-ttu-id="712f2-124">沒有</span><span class="sxs-lookup"><span data-stu-id="712f2-124">None</span></span>

## <span data-ttu-id="712f2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="712f2-125">OUTPUTS</span></span>

### <span data-ttu-id="712f2-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="712f2-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="712f2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="712f2-127">NOTES</span></span>

## <span data-ttu-id="712f2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="712f2-128">RELATED LINKS</span></span>

[<span data-ttu-id="712f2-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="712f2-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="712f2-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="712f2-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="712f2-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="712f2-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)