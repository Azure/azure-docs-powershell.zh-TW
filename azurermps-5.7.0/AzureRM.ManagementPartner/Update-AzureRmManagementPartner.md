---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 9d1694cdde3edd94112fc5b1960fd870b842d6e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624490"
---
# <span data-ttu-id="e70a7-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e70a7-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="e70a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e70a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e70a7-103">更新 Microsoft 合作夥伴網路 (MPN 目前已驗證的使用者或服務主體) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e70a7-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e70a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="e70a7-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70a7-105">說明</span><span class="sxs-lookup"><span data-stu-id="e70a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e70a7-106">更新 Microsoft 合作夥伴網路 (MPN 目前已驗證的使用者或服務主體) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e70a7-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e70a7-107">示例</span><span class="sxs-lookup"><span data-stu-id="e70a7-107">EXAMPLES</span></span>

### <span data-ttu-id="e70a7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e70a7-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="e70a7-109">將管理合作夥伴更新為新的管理夥伴</span><span class="sxs-lookup"><span data-stu-id="e70a7-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="e70a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="e70a7-110">PARAMETERS</span></span>

### <span data-ttu-id="e70a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70a7-111">-DefaultProfile</span></span>
<span data-ttu-id="e70a7-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e70a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70a7-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="e70a7-113">-PartnerId</span></span>
<span data-ttu-id="e70a7-114">管理合作夥伴識別碼，它是6位數的數位</span><span class="sxs-lookup"><span data-stu-id="e70a7-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70a7-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e70a7-115">-Confirm</span></span>
<span data-ttu-id="e70a7-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e70a7-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70a7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70a7-117">-WhatIf</span></span>
<span data-ttu-id="e70a7-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e70a7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e70a7-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e70a7-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70a7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70a7-120">CommonParameters</span></span>
<span data-ttu-id="e70a7-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e70a7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70a7-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e70a7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70a7-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e70a7-123">INPUTS</span></span>

### <span data-ttu-id="e70a7-124">所有</span><span class="sxs-lookup"><span data-stu-id="e70a7-124">None</span></span>

## <span data-ttu-id="e70a7-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e70a7-125">OUTPUTS</span></span>

### <span data-ttu-id="e70a7-126">PSManagementPartner 的資源。</span><span class="sxs-lookup"><span data-stu-id="e70a7-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="e70a7-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e70a7-127">NOTES</span></span>

## <span data-ttu-id="e70a7-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e70a7-128">RELATED LINKS</span></span>

[<span data-ttu-id="e70a7-129">移除-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e70a7-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="e70a7-130">新-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e70a7-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="e70a7-131">AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e70a7-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
