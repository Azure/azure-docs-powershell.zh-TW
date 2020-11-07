---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 5910d82ddee49ba47c709a3323f72e325f4067ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786881"
---
# <span data-ttu-id="0bab1-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0bab1-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="0bab1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bab1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bab1-103">刪除 [Microsoft 合作夥伴網路] (MPN 目前已驗證驗證的使用者或服務主體的) ID。</span><span class="sxs-lookup"><span data-stu-id="0bab1-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0bab1-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bab1-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bab1-105">說明</span><span class="sxs-lookup"><span data-stu-id="0bab1-105">DESCRIPTION</span></span>
<span data-ttu-id="0bab1-106">刪除 [Microsoft 合作夥伴網路] (MPN 目前已驗證驗證的使用者或服務主體的) ID。</span><span class="sxs-lookup"><span data-stu-id="0bab1-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0bab1-107">示例</span><span class="sxs-lookup"><span data-stu-id="0bab1-107">EXAMPLES</span></span>

### <span data-ttu-id="0bab1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0bab1-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="0bab1-109">移除管理合作夥伴</span><span class="sxs-lookup"><span data-stu-id="0bab1-109">Remove management partner</span></span>

## <span data-ttu-id="0bab1-110">參數</span><span class="sxs-lookup"><span data-stu-id="0bab1-110">PARAMETERS</span></span>

### <span data-ttu-id="0bab1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bab1-111">-DefaultProfile</span></span>
<span data-ttu-id="0bab1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bab1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bab1-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0bab1-113">-PartnerId</span></span>
<span data-ttu-id="0bab1-114">管理合作夥伴識別碼，它是6位數的數位</span><span class="sxs-lookup"><span data-stu-id="0bab1-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="0bab1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bab1-115">-PassThru</span></span>
<span data-ttu-id="0bab1-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="0bab1-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0bab1-117">-確認</span><span class="sxs-lookup"><span data-stu-id="0bab1-117">-Confirm</span></span>
<span data-ttu-id="0bab1-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0bab1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bab1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bab1-119">-WhatIf</span></span>
<span data-ttu-id="0bab1-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0bab1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bab1-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0bab1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bab1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bab1-122">CommonParameters</span></span>
<span data-ttu-id="0bab1-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bab1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bab1-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bab1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bab1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0bab1-125">INPUTS</span></span>

### <span data-ttu-id="0bab1-126">所有</span><span class="sxs-lookup"><span data-stu-id="0bab1-126">None</span></span>

## <span data-ttu-id="0bab1-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0bab1-127">OUTPUTS</span></span>

### <span data-ttu-id="0bab1-128">System.object</span><span class="sxs-lookup"><span data-stu-id="0bab1-128">System.Boolean</span></span>

## <span data-ttu-id="0bab1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0bab1-129">NOTES</span></span>

## <span data-ttu-id="0bab1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bab1-130">RELATED LINKS</span></span>

[<span data-ttu-id="0bab1-131">新-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0bab1-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="0bab1-132">AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0bab1-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="0bab1-133">更新-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0bab1-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)