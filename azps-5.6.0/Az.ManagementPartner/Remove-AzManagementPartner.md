---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 7a213cbe8acacebc0f6e513e264432ca2ba08cf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911645"
---
# <span data-ttu-id="777dd-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="777dd-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="777dd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="777dd-102">SYNOPSIS</span></span>
<span data-ttu-id="777dd-103">刪除 Microsoft 合作夥伴網路 (MPN) 驗證之使用者或服務主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="777dd-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="777dd-104">語法</span><span class="sxs-lookup"><span data-stu-id="777dd-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="777dd-105">描述</span><span class="sxs-lookup"><span data-stu-id="777dd-105">DESCRIPTION</span></span>
<span data-ttu-id="777dd-106">刪除 Microsoft 合作夥伴網路 (MPN) 驗證之使用者或服務主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="777dd-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="777dd-107">例子</span><span class="sxs-lookup"><span data-stu-id="777dd-107">EXAMPLES</span></span>

### <span data-ttu-id="777dd-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="777dd-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="777dd-109">移除管理合作夥伴</span><span class="sxs-lookup"><span data-stu-id="777dd-109">Remove management partner</span></span>

## <span data-ttu-id="777dd-110">參數</span><span class="sxs-lookup"><span data-stu-id="777dd-110">PARAMETERS</span></span>

### <span data-ttu-id="777dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="777dd-111">-DefaultProfile</span></span>
<span data-ttu-id="777dd-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="777dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="777dd-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="777dd-113">-PartnerId</span></span>
<span data-ttu-id="777dd-114">管理合作夥伴識別碼，這是 6 位數的數位</span><span class="sxs-lookup"><span data-stu-id="777dd-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="777dd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="777dd-115">-PassThru</span></span>
<span data-ttu-id="777dd-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="777dd-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="777dd-117">-確認</span><span class="sxs-lookup"><span data-stu-id="777dd-117">-Confirm</span></span>
<span data-ttu-id="777dd-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="777dd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="777dd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="777dd-119">-WhatIf</span></span>
<span data-ttu-id="777dd-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="777dd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="777dd-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="777dd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="777dd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777dd-122">CommonParameters</span></span>
<span data-ttu-id="777dd-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="777dd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777dd-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="777dd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777dd-125">輸入</span><span class="sxs-lookup"><span data-stu-id="777dd-125">INPUTS</span></span>

### <span data-ttu-id="777dd-126">沒有</span><span class="sxs-lookup"><span data-stu-id="777dd-126">None</span></span>

## <span data-ttu-id="777dd-127">輸出</span><span class="sxs-lookup"><span data-stu-id="777dd-127">OUTPUTS</span></span>

### <span data-ttu-id="777dd-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="777dd-128">System.Boolean</span></span>

## <span data-ttu-id="777dd-129">筆記</span><span class="sxs-lookup"><span data-stu-id="777dd-129">NOTES</span></span>

## <span data-ttu-id="777dd-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="777dd-130">RELATED LINKS</span></span>

[<span data-ttu-id="777dd-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="777dd-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="777dd-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="777dd-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="777dd-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="777dd-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)