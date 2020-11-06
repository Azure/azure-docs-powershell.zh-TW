---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5604430c795f7a318e18b89928c3a75d063a316a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448708"
---
# <span data-ttu-id="8e554-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8e554-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8e554-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e554-102">SYNOPSIS</span></span>
<span data-ttu-id="8e554-103">移除指定的 Azure Data Lake Analytics 計算原則</span><span class="sxs-lookup"><span data-stu-id="8e554-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e554-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e554-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e554-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e554-105">DESCRIPTION</span></span>
<span data-ttu-id="8e554-106">**移除-AzureRmDataLakeAnalyticsComputePolicy** 會移除指定的 Azure Data Lake Analytics 計算原則。</span><span class="sxs-lookup"><span data-stu-id="8e554-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="8e554-107">示例</span><span class="sxs-lookup"><span data-stu-id="8e554-107">EXAMPLES</span></span>

### <span data-ttu-id="8e554-108">範例1：移除計算原則</span><span class="sxs-lookup"><span data-stu-id="8e554-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="8e554-109">此命令會移除帳戶 "contosoadla" 中名為 "myPolicy" 的指定計算原則。</span><span class="sxs-lookup"><span data-stu-id="8e554-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="8e554-110">參數</span><span class="sxs-lookup"><span data-stu-id="8e554-110">PARAMETERS</span></span>

### <span data-ttu-id="8e554-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="8e554-111">-Account</span></span>
<span data-ttu-id="8e554-112">要移除其計算原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8e554-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e554-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e554-113">-DefaultProfile</span></span>
<span data-ttu-id="8e554-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8e554-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e554-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e554-115">-Name</span></span>
<span data-ttu-id="8e554-116">要移除之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e554-116">Name of the compute policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e554-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e554-117">-PassThru</span></span>
<span data-ttu-id="8e554-118">成功刪除時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="8e554-118">Return true upon successful deletion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e554-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e554-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e554-120">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e554-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="8e554-121">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="8e554-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e554-122">-確認</span><span class="sxs-lookup"><span data-stu-id="8e554-122">-Confirm</span></span>
<span data-ttu-id="8e554-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e554-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e554-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e554-124">-WhatIf</span></span>
<span data-ttu-id="8e554-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e554-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e554-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e554-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e554-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e554-127">CommonParameters</span></span>
<span data-ttu-id="8e554-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e554-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e554-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e554-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e554-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8e554-130">INPUTS</span></span>

### <span data-ttu-id="8e554-131">System.object</span><span class="sxs-lookup"><span data-stu-id="8e554-131">System.String</span></span>

## <span data-ttu-id="8e554-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8e554-132">OUTPUTS</span></span>

### <span data-ttu-id="8e554-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8e554-133">System.Boolean</span></span>

## <span data-ttu-id="8e554-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8e554-134">NOTES</span></span>

## <span data-ttu-id="8e554-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e554-135">RELATED LINKS</span></span>

