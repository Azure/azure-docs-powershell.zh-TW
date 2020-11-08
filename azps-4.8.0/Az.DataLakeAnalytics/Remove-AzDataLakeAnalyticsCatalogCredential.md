---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969313"
---
# <span data-ttu-id="e1be4-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="e1be4-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="e1be4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1be4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1be4-103">刪除 Azure Data Lake Analytics 認證。</span><span class="sxs-lookup"><span data-stu-id="e1be4-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="e1be4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1be4-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1be4-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1be4-105">DESCRIPTION</span></span>
<span data-ttu-id="e1be4-106">Remove-AzDataLakeAnalyticsCatalogCredential Cmdlet 會刪除 Azure Data Lake Analytics 目錄認證。</span><span class="sxs-lookup"><span data-stu-id="e1be4-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="e1be4-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1be4-107">EXAMPLES</span></span>

### <span data-ttu-id="e1be4-108">範例1：移除認證</span><span class="sxs-lookup"><span data-stu-id="e1be4-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="e1be4-109">這個命令會移除指定的資料 Lake Analytics 編目認證。</span><span class="sxs-lookup"><span data-stu-id="e1be4-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="e1be4-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1be4-110">PARAMETERS</span></span>

### <span data-ttu-id="e1be4-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e1be4-111">-Account</span></span>
<span data-ttu-id="e1be4-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e1be4-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e1be4-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1be4-113">-DatabaseName</span></span>
<span data-ttu-id="e1be4-114">指定儲存認證的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e1be4-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="e1be4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1be4-115">-DefaultProfile</span></span>
<span data-ttu-id="e1be4-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e1be4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1be4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e1be4-117">-Force</span></span>
<span data-ttu-id="e1be4-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e1be4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1be4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1be4-119">-Name</span></span>
<span data-ttu-id="e1be4-120">指定認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1be4-120">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1be4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1be4-121">-PassThru</span></span>
<span data-ttu-id="e1be4-122">表示此 Cmdlet 不會等待操作完成。</span><span class="sxs-lookup"><span data-stu-id="e1be4-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="e1be4-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e1be4-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1be4-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e1be4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1be4-125">-Password</span><span class="sxs-lookup"><span data-stu-id="e1be4-125">-Password</span></span>
<span data-ttu-id="e1be4-126">認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="e1be4-126">The password for the credential.</span></span>
<span data-ttu-id="e1be4-127">如果來電者不是帳戶的擁有者，則需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="e1be4-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1be4-128">-遞迴</span><span class="sxs-lookup"><span data-stu-id="e1be4-128">-Recurse</span></span>
<span data-ttu-id="e1be4-129">表示此刪除操作應該經過，而且也會刪除並丟棄所有依存于此認證的資源。</span><span class="sxs-lookup"><span data-stu-id="e1be4-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1be4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="e1be4-130">-Confirm</span></span>
<span data-ttu-id="e1be4-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1be4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1be4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1be4-132">-WhatIf</span></span>
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

### <span data-ttu-id="e1be4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1be4-133">CommonParameters</span></span>
<span data-ttu-id="e1be4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1be4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1be4-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1be4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1be4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e1be4-136">INPUTS</span></span>

### <span data-ttu-id="e1be4-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e1be4-137">System.String</span></span>

### <span data-ttu-id="e1be4-138">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="e1be4-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="e1be4-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e1be4-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1be4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e1be4-140">OUTPUTS</span></span>

### <span data-ttu-id="e1be4-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e1be4-141">System.Boolean</span></span>

## <span data-ttu-id="e1be4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e1be4-142">NOTES</span></span>

## <span data-ttu-id="e1be4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1be4-143">RELATED LINKS</span></span>
