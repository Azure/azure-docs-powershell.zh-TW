---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 3bb1b54abf947d5fc2a05538cc31ce53fb794ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455243"
---
# <span data-ttu-id="2d4e8-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2d4e8-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="2d4e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4e8-103">刪除 [Microsoft 合作夥伴網路] (MPN 目前已驗證驗證的使用者或服務主體的) ID。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d4e8-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d4e8-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4e8-106">刪除 [Microsoft 合作夥伴網路] (MPN 目前已驗證驗證的使用者或服務主體的) ID。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="2d4e8-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d4e8-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4e8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2d4e8-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="2d4e8-109">移除管理合作夥伴</span><span class="sxs-lookup"><span data-stu-id="2d4e8-109">Remove management partner</span></span> 

## <span data-ttu-id="2d4e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d4e8-110">PARAMETERS</span></span>

### <span data-ttu-id="2d4e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4e8-111">-DefaultProfile</span></span>
<span data-ttu-id="2d4e8-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e8-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="2d4e8-113">-PartnerId</span></span>
<span data-ttu-id="2d4e8-114">管理合作夥伴識別碼，它是6位數的數位</span><span class="sxs-lookup"><span data-stu-id="2d4e8-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="2d4e8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d4e8-115">-PassThru</span></span>
<span data-ttu-id="2d4e8-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="2d4e8-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2d4e8-117">-確認</span><span class="sxs-lookup"><span data-stu-id="2d4e8-117">-Confirm</span></span>
<span data-ttu-id="2d4e8-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4e8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4e8-119">-WhatIf</span></span>
<span data-ttu-id="2d4e8-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d4e8-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4e8-122">CommonParameters</span></span>
<span data-ttu-id="2d4e8-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4e8-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d4e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4e8-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2d4e8-125">INPUTS</span></span>

### <span data-ttu-id="2d4e8-126">所有</span><span class="sxs-lookup"><span data-stu-id="2d4e8-126">None</span></span>

## <span data-ttu-id="2d4e8-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2d4e8-127">OUTPUTS</span></span>

### <span data-ttu-id="2d4e8-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2d4e8-128">System.Boolean</span></span>

## <span data-ttu-id="2d4e8-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2d4e8-129">NOTES</span></span>

## <span data-ttu-id="2d4e8-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d4e8-130">RELATED LINKS</span></span>

[<span data-ttu-id="2d4e8-131">新-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2d4e8-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="2d4e8-132">AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2d4e8-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="2d4e8-133">更新-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2d4e8-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
