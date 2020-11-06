---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452192"
---
# <span data-ttu-id="40606-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="40606-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="40606-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40606-102">SYNOPSIS</span></span>
<span data-ttu-id="40606-103">將 Microsoft Partner Network (MPN) 識別碼與目前已驗證身份的使用者或服務主體相關聯。</span><span class="sxs-lookup"><span data-stu-id="40606-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40606-104">句法</span><span class="sxs-lookup"><span data-stu-id="40606-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40606-105">說明</span><span class="sxs-lookup"><span data-stu-id="40606-105">DESCRIPTION</span></span>
<span data-ttu-id="40606-106">將 Microsoft Partner Network (MPN) 識別碼與目前已驗證身份的使用者或服務主體相關聯。</span><span class="sxs-lookup"><span data-stu-id="40606-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="40606-107">示例</span><span class="sxs-lookup"><span data-stu-id="40606-107">EXAMPLES</span></span>

### <span data-ttu-id="40606-108">範例1</span><span class="sxs-lookup"><span data-stu-id="40606-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="40606-109">新增管理合作夥伴</span><span class="sxs-lookup"><span data-stu-id="40606-109">Add a management partner</span></span> 

## <span data-ttu-id="40606-110">參數</span><span class="sxs-lookup"><span data-stu-id="40606-110">PARAMETERS</span></span>

### <span data-ttu-id="40606-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40606-111">-DefaultProfile</span></span>
<span data-ttu-id="40606-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40606-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40606-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="40606-113">-PartnerId</span></span>
<span data-ttu-id="40606-114">管理合作夥伴識別碼，它是6位數的數位</span><span class="sxs-lookup"><span data-stu-id="40606-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="40606-115">-確認</span><span class="sxs-lookup"><span data-stu-id="40606-115">-Confirm</span></span>
<span data-ttu-id="40606-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40606-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40606-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40606-117">-WhatIf</span></span>
<span data-ttu-id="40606-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40606-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40606-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40606-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40606-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40606-120">CommonParameters</span></span>
<span data-ttu-id="40606-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40606-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40606-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40606-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40606-123">輸入</span><span class="sxs-lookup"><span data-stu-id="40606-123">INPUTS</span></span>

### <span data-ttu-id="40606-124">所有</span><span class="sxs-lookup"><span data-stu-id="40606-124">None</span></span>

## <span data-ttu-id="40606-125">輸出</span><span class="sxs-lookup"><span data-stu-id="40606-125">OUTPUTS</span></span>

### <span data-ttu-id="40606-126">PSManagementPartner 的資源。</span><span class="sxs-lookup"><span data-stu-id="40606-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="40606-127">筆記</span><span class="sxs-lookup"><span data-stu-id="40606-127">NOTES</span></span>

## <span data-ttu-id="40606-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="40606-128">RELATED LINKS</span></span>

[<span data-ttu-id="40606-129">移除-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="40606-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="40606-130">AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="40606-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="40606-131">更新-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="40606-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
