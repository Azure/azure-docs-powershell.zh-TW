---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 29846c8bb5650a667bf565fec273cbf24c8cd394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915518"
---
# <span data-ttu-id="b2ce2-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2ce2-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="b2ce2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b2ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ce2-103">刪除 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="b2ce2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b2ce2-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2ce2-105">描述</span><span class="sxs-lookup"><span data-stu-id="b2ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="b2ce2-106">**Remove-AzDataLakeAnalyticsAccount** Cmdlet 會永久刪除 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="b2ce2-107">例子</span><span class="sxs-lookup"><span data-stu-id="b2ce2-107">EXAMPLES</span></span>

### <span data-ttu-id="b2ce2-108">範例 1：移除帳戶</span><span class="sxs-lookup"><span data-stu-id="b2ce2-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="b2ce2-109">此命令會移除指定的 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="b2ce2-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2ce2-110">PARAMETERS</span></span>

### <span data-ttu-id="b2ce2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ce2-111">-DefaultProfile</span></span>
<span data-ttu-id="b2ce2-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b2ce2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2ce2-113">-強制</span><span class="sxs-lookup"><span data-stu-id="b2ce2-113">-Force</span></span>
<span data-ttu-id="b2ce2-114">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ce2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2ce2-115">-Name</span></span>
<span data-ttu-id="b2ce2-116">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ce2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2ce2-117">-PassThru</span></span>
<span data-ttu-id="b2ce2-118">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b2ce2-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ce2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ce2-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2ce2-121">指定 Data Lake Analytics 帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ce2-122">-確認</span><span class="sxs-lookup"><span data-stu-id="b2ce2-122">-Confirm</span></span>
<span data-ttu-id="b2ce2-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ce2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2ce2-124">-WhatIf</span></span>
<span data-ttu-id="b2ce2-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2ce2-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ce2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ce2-127">CommonParameters</span></span>
<span data-ttu-id="b2ce2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ce2-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b2ce2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ce2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b2ce2-130">INPUTS</span></span>

### <span data-ttu-id="b2ce2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b2ce2-131">System.String</span></span>

## <span data-ttu-id="b2ce2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b2ce2-132">OUTPUTS</span></span>

### <span data-ttu-id="b2ce2-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2ce2-133">System.Boolean</span></span>

## <span data-ttu-id="b2ce2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b2ce2-134">NOTES</span></span>

## <span data-ttu-id="b2ce2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2ce2-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2ce2-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2ce2-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b2ce2-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2ce2-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b2ce2-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2ce2-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b2ce2-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2ce2-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


