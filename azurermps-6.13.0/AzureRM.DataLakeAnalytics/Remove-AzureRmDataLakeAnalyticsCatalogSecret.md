---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: aa7dace3141210e8c4ff6055a011f34523c5b586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447380"
---
# <span data-ttu-id="00fde-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="00fde-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="00fde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00fde-102">SYNOPSIS</span></span>
<span data-ttu-id="00fde-103">刪除 Data Lake Analytics 密碼。</span><span class="sxs-lookup"><span data-stu-id="00fde-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00fde-104">句法</span><span class="sxs-lookup"><span data-stu-id="00fde-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00fde-105">說明</span><span class="sxs-lookup"><span data-stu-id="00fde-105">DESCRIPTION</span></span>
<span data-ttu-id="00fde-106">**AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet 會刪除 Azure Data Lake Analytics 目錄機密。</span><span class="sxs-lookup"><span data-stu-id="00fde-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="00fde-107">示例</span><span class="sxs-lookup"><span data-stu-id="00fde-107">EXAMPLES</span></span>

### <span data-ttu-id="00fde-108">範例1：移除機密</span><span class="sxs-lookup"><span data-stu-id="00fde-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="00fde-109">這個命令會移除指定的資料 Lake Analytics 目錄機密。</span><span class="sxs-lookup"><span data-stu-id="00fde-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="00fde-110">參數</span><span class="sxs-lookup"><span data-stu-id="00fde-110">PARAMETERS</span></span>

### <span data-ttu-id="00fde-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="00fde-111">-Account</span></span>
<span data-ttu-id="00fde-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="00fde-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="00fde-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00fde-113">-DatabaseName</span></span>
<span data-ttu-id="00fde-114">指定儲存秘密之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="00fde-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="00fde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fde-115">-DefaultProfile</span></span>
<span data-ttu-id="00fde-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="00fde-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00fde-117">-Force</span><span class="sxs-lookup"><span data-stu-id="00fde-117">-Force</span></span>
<span data-ttu-id="00fde-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="00fde-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00fde-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="00fde-119">-Name</span></span>
<span data-ttu-id="00fde-120">指定密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="00fde-120">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="00fde-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00fde-121">-PassThru</span></span>
<span data-ttu-id="00fde-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="00fde-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00fde-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="00fde-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="00fde-124">-確認</span><span class="sxs-lookup"><span data-stu-id="00fde-124">-Confirm</span></span>
<span data-ttu-id="00fde-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00fde-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fde-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fde-126">-WhatIf</span></span>
<span data-ttu-id="00fde-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00fde-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fde-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00fde-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fde-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fde-129">CommonParameters</span></span>
<span data-ttu-id="00fde-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00fde-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fde-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00fde-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fde-132">輸入</span><span class="sxs-lookup"><span data-stu-id="00fde-132">INPUTS</span></span>

### <span data-ttu-id="00fde-133">System.object</span><span class="sxs-lookup"><span data-stu-id="00fde-133">System.String</span></span>

## <span data-ttu-id="00fde-134">輸出</span><span class="sxs-lookup"><span data-stu-id="00fde-134">OUTPUTS</span></span>

### <span data-ttu-id="00fde-135">System.object</span><span class="sxs-lookup"><span data-stu-id="00fde-135">System.Boolean</span></span>

## <span data-ttu-id="00fde-136">筆記</span><span class="sxs-lookup"><span data-stu-id="00fde-136">NOTES</span></span>

## <span data-ttu-id="00fde-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="00fde-137">RELATED LINKS</span></span>

[<span data-ttu-id="00fde-138">新-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="00fde-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="00fde-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="00fde-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


