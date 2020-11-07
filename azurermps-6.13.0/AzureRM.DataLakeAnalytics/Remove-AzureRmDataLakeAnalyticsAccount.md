---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a04295bca6c664e583ae9653b1f3ed7d52aebf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625311"
---
# <span data-ttu-id="552f8-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="552f8-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="552f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="552f8-102">SYNOPSIS</span></span>
<span data-ttu-id="552f8-103">刪除 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="552f8-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="552f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="552f8-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="552f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="552f8-105">DESCRIPTION</span></span>
<span data-ttu-id="552f8-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet 會永久刪除 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="552f8-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="552f8-107">示例</span><span class="sxs-lookup"><span data-stu-id="552f8-107">EXAMPLES</span></span>

### <span data-ttu-id="552f8-108">範例1：移除帳戶</span><span class="sxs-lookup"><span data-stu-id="552f8-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="552f8-109">這個命令會移除指定的資料 Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="552f8-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="552f8-110">參數</span><span class="sxs-lookup"><span data-stu-id="552f8-110">PARAMETERS</span></span>

### <span data-ttu-id="552f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="552f8-111">-DefaultProfile</span></span>
<span data-ttu-id="552f8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="552f8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="552f8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="552f8-113">-Force</span></span>
<span data-ttu-id="552f8-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="552f8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="552f8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="552f8-115">-Name</span></span>
<span data-ttu-id="552f8-116">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="552f8-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="552f8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="552f8-117">-PassThru</span></span>
<span data-ttu-id="552f8-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="552f8-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="552f8-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="552f8-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="552f8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="552f8-120">-ResourceGroupName</span></span>
<span data-ttu-id="552f8-121">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="552f8-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="552f8-122">-確認</span><span class="sxs-lookup"><span data-stu-id="552f8-122">-Confirm</span></span>
<span data-ttu-id="552f8-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="552f8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="552f8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="552f8-124">-WhatIf</span></span>
<span data-ttu-id="552f8-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="552f8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="552f8-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="552f8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="552f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="552f8-127">CommonParameters</span></span>
<span data-ttu-id="552f8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="552f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="552f8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="552f8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="552f8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="552f8-130">INPUTS</span></span>

### <span data-ttu-id="552f8-131">System.object</span><span class="sxs-lookup"><span data-stu-id="552f8-131">System.String</span></span>

## <span data-ttu-id="552f8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="552f8-132">OUTPUTS</span></span>

### <span data-ttu-id="552f8-133">System.object</span><span class="sxs-lookup"><span data-stu-id="552f8-133">System.Boolean</span></span>

## <span data-ttu-id="552f8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="552f8-134">NOTES</span></span>

## <span data-ttu-id="552f8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="552f8-135">RELATED LINKS</span></span>

[<span data-ttu-id="552f8-136">AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="552f8-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="552f8-137">新-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="552f8-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="552f8-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="552f8-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="552f8-139">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="552f8-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


