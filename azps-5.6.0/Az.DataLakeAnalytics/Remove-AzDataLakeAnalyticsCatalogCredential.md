---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: f14448e7b7606f37f5ffdee8c944d48a557c1f0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914018"
---
# <span data-ttu-id="c3831-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="c3831-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="c3831-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c3831-102">SYNOPSIS</span></span>
<span data-ttu-id="c3831-103">刪除 Azure Data Lake Analytics 認證。</span><span class="sxs-lookup"><span data-stu-id="c3831-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="c3831-104">語法</span><span class="sxs-lookup"><span data-stu-id="c3831-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3831-105">描述</span><span class="sxs-lookup"><span data-stu-id="c3831-105">DESCRIPTION</span></span>
<span data-ttu-id="c3831-106">Cmdlet Remove-AzDataLakeAnalyticsCatalogCredential Azure Data Lake Analytics 目錄認證。</span><span class="sxs-lookup"><span data-stu-id="c3831-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="c3831-107">例子</span><span class="sxs-lookup"><span data-stu-id="c3831-107">EXAMPLES</span></span>

### <span data-ttu-id="c3831-108">範例 1：移除認證</span><span class="sxs-lookup"><span data-stu-id="c3831-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="c3831-109">此命令會移除指定的 Data Lake Analytics 目錄認證。</span><span class="sxs-lookup"><span data-stu-id="c3831-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="c3831-110">參數</span><span class="sxs-lookup"><span data-stu-id="c3831-110">PARAMETERS</span></span>

### <span data-ttu-id="c3831-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c3831-111">-Account</span></span>
<span data-ttu-id="c3831-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c3831-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c3831-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c3831-113">-DatabaseName</span></span>
<span data-ttu-id="c3831-114">指定保留該認證的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c3831-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="c3831-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3831-115">-DefaultProfile</span></span>
<span data-ttu-id="c3831-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c3831-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3831-117">-強制</span><span class="sxs-lookup"><span data-stu-id="c3831-117">-Force</span></span>
<span data-ttu-id="c3831-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c3831-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3831-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3831-119">-Name</span></span>
<span data-ttu-id="c3831-120">指定認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3831-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="c3831-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3831-121">-PassThru</span></span>
<span data-ttu-id="c3831-122">表示此 Cmdlet 不會等待作業完成。</span><span class="sxs-lookup"><span data-stu-id="c3831-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="c3831-123">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c3831-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c3831-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c3831-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3831-125">-密碼</span><span class="sxs-lookup"><span data-stu-id="c3831-125">-Password</span></span>
<span data-ttu-id="c3831-126">認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="c3831-126">The password for the credential.</span></span>
<span data-ttu-id="c3831-127">如果來電者不是帳戶的擁有者，則此為必填專案。</span><span class="sxs-lookup"><span data-stu-id="c3831-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="c3831-128">-遞迴</span><span class="sxs-lookup"><span data-stu-id="c3831-128">-Recurse</span></span>
<span data-ttu-id="c3831-129">表示此刪除作業應該執行，也會刪除和刪除所有依存于此認證的資源。</span><span class="sxs-lookup"><span data-stu-id="c3831-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="c3831-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c3831-130">-Confirm</span></span>
<span data-ttu-id="c3831-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c3831-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3831-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3831-132">-WhatIf</span></span>
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

### <span data-ttu-id="c3831-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3831-133">CommonParameters</span></span>
<span data-ttu-id="c3831-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c3831-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3831-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c3831-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3831-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c3831-136">INPUTS</span></span>

### <span data-ttu-id="c3831-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c3831-137">System.String</span></span>

### <span data-ttu-id="c3831-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="c3831-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="c3831-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3831-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3831-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c3831-140">OUTPUTS</span></span>

### <span data-ttu-id="c3831-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3831-141">System.Boolean</span></span>

## <span data-ttu-id="c3831-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c3831-142">NOTES</span></span>

## <span data-ttu-id="c3831-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3831-143">RELATED LINKS</span></span>
