---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625219"
---
# <span data-ttu-id="e746d-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e746d-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="e746d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e746d-102">SYNOPSIS</span></span>
<span data-ttu-id="e746d-103">刪除 Data Lake Analytics 密碼。</span><span class="sxs-lookup"><span data-stu-id="e746d-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e746d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e746d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e746d-105">說明</span><span class="sxs-lookup"><span data-stu-id="e746d-105">DESCRIPTION</span></span>
<span data-ttu-id="e746d-106">**AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet 會刪除 Azure Data Lake Analytics 目錄機密。</span><span class="sxs-lookup"><span data-stu-id="e746d-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="e746d-107">示例</span><span class="sxs-lookup"><span data-stu-id="e746d-107">EXAMPLES</span></span>

### <span data-ttu-id="e746d-108">範例1：移除機密</span><span class="sxs-lookup"><span data-stu-id="e746d-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="e746d-109">這個命令會移除指定的資料 Lake Analytics 目錄機密。</span><span class="sxs-lookup"><span data-stu-id="e746d-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="e746d-110">參數</span><span class="sxs-lookup"><span data-stu-id="e746d-110">PARAMETERS</span></span>

### <span data-ttu-id="e746d-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e746d-111">-Account</span></span>
<span data-ttu-id="e746d-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e746d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e746d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e746d-113">-DatabaseName</span></span>
<span data-ttu-id="e746d-114">指定儲存秘密之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e746d-114">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e746d-115">-Force</span></span>
<span data-ttu-id="e746d-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e746d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e746d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e746d-117">-Name</span></span>
<span data-ttu-id="e746d-118">指定密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="e746d-118">Specifies the name of the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e746d-119">-PassThru</span></span>
<span data-ttu-id="e746d-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e746d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e746d-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e746d-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-122">-確認</span><span class="sxs-lookup"><span data-stu-id="e746d-122">-Confirm</span></span>
<span data-ttu-id="e746d-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e746d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e746d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e746d-124">-WhatIf</span></span>
<span data-ttu-id="e746d-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e746d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e746d-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e746d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e746d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e746d-127">-DefaultProfile</span></span>
<span data-ttu-id="e746d-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e746d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e746d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e746d-129">CommonParameters</span></span>
<span data-ttu-id="e746d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e746d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e746d-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e746d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e746d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e746d-132">INPUTS</span></span>

## <span data-ttu-id="e746d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e746d-133">OUTPUTS</span></span>

### <span data-ttu-id="e746d-134">bool</span><span class="sxs-lookup"><span data-stu-id="e746d-134">bool</span></span>
<span data-ttu-id="e746d-135">如果已指定 PassThru，則會在作業完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e746d-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="e746d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e746d-136">NOTES</span></span>

## <span data-ttu-id="e746d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e746d-137">RELATED LINKS</span></span>

[<span data-ttu-id="e746d-138">新-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e746d-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="e746d-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e746d-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


