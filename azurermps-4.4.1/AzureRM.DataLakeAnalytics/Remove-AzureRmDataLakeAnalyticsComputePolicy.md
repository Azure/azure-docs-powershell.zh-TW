---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453564"
---
# <span data-ttu-id="1ad80-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1ad80-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1ad80-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ad80-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad80-103">移除指定的 Azure Data Lake Analytics 計算原則</span><span class="sxs-lookup"><span data-stu-id="1ad80-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ad80-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ad80-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad80-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ad80-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad80-106">**移除-AzureRmDataLakeAnalyticsComputePolicy** 會移除指定的 Azure Data Lake Analytics 計算原則。</span><span class="sxs-lookup"><span data-stu-id="1ad80-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="1ad80-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ad80-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad80-108">範例1：移除計算原則</span><span class="sxs-lookup"><span data-stu-id="1ad80-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="1ad80-109">此命令會移除帳戶 "contosoadla" 中名為 "myPolicy" 的指定計算原則。</span><span class="sxs-lookup"><span data-stu-id="1ad80-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="1ad80-110">參數</span><span class="sxs-lookup"><span data-stu-id="1ad80-110">PARAMETERS</span></span>

### <span data-ttu-id="1ad80-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="1ad80-111">-Account</span></span>
<span data-ttu-id="1ad80-112">要移除其計算原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad80-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad80-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ad80-113">-Name</span></span>
<span data-ttu-id="1ad80-114">要移除之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad80-114">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad80-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ad80-115">-PassThru</span></span>
<span data-ttu-id="1ad80-116">成功刪除時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="1ad80-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="1ad80-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad80-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ad80-118">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad80-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="1ad80-119">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="1ad80-119">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad80-120">-確認</span><span class="sxs-lookup"><span data-stu-id="1ad80-120">-Confirm</span></span>
<span data-ttu-id="1ad80-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ad80-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad80-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad80-122">-WhatIf</span></span>
<span data-ttu-id="1ad80-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ad80-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad80-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ad80-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad80-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad80-125">-DefaultProfile</span></span>
<span data-ttu-id="1ad80-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ad80-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ad80-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad80-127">CommonParameters</span></span>
<span data-ttu-id="1ad80-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ad80-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad80-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ad80-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad80-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1ad80-130">INPUTS</span></span>

### <span data-ttu-id="1ad80-131">System.object</span><span class="sxs-lookup"><span data-stu-id="1ad80-131">System.String</span></span>

## <span data-ttu-id="1ad80-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1ad80-132">OUTPUTS</span></span>

### <span data-ttu-id="1ad80-133">System.object</span><span class="sxs-lookup"><span data-stu-id="1ad80-133">System.Boolean</span></span>

## <span data-ttu-id="1ad80-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1ad80-134">NOTES</span></span>

## <span data-ttu-id="1ad80-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ad80-135">RELATED LINKS</span></span>

