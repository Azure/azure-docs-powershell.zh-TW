---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7af5736e2f66b8bf428815456ba95b3c5b4b6182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623788"
---
# <span data-ttu-id="f675b-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f675b-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f675b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f675b-102">SYNOPSIS</span></span>
<span data-ttu-id="f675b-103">修改 Azure SQL Database Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="f675b-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f675b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f675b-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f675b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f675b-105">DESCRIPTION</span></span>
<span data-ttu-id="f675b-106">**AzureRmSqlDatabaseAdvisorAutoExecuteStatus** Cmdlet 會修改 Azure SQL Database Advisor 的自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="f675b-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="f675b-107">這個 Cmdlet 目前支援啟用、停用和預設值。</span><span class="sxs-lookup"><span data-stu-id="f675b-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="f675b-108">示例</span><span class="sxs-lookup"><span data-stu-id="f675b-108">EXAMPLES</span></span>

### <span data-ttu-id="f675b-109">範例1：啟用 advisor 的自動執行</span><span class="sxs-lookup"><span data-stu-id="f675b-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="f675b-110">這個命令會將名為 CreateIndex 的 advisor 的自動執行狀態變更為 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="f675b-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="f675b-111">參數</span><span class="sxs-lookup"><span data-stu-id="f675b-111">PARAMETERS</span></span>

### <span data-ttu-id="f675b-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f675b-112">-AdvisorName</span></span>
<span data-ttu-id="f675b-113">指定此 Cmdlet 修改狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="f675b-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f675b-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f675b-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="f675b-115">指定狀態的值。</span><span class="sxs-lookup"><span data-stu-id="f675b-115">Specifies the value for the status.</span></span>
<span data-ttu-id="f675b-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f675b-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f675b-117">後</span><span class="sxs-lookup"><span data-stu-id="f675b-117">Enabled</span></span> 
- <span data-ttu-id="f675b-118">禁止</span><span class="sxs-lookup"><span data-stu-id="f675b-118">Disabled</span></span> 
- <span data-ttu-id="f675b-119">設置</span><span class="sxs-lookup"><span data-stu-id="f675b-119">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f675b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f675b-120">-DatabaseName</span></span>
<span data-ttu-id="f675b-121">指定此 Cmdlet 修改狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f675b-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f675b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f675b-122">-DefaultProfile</span></span>
<span data-ttu-id="f675b-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f675b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f675b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f675b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f675b-125">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f675b-125">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f675b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f675b-126">-ServerName</span></span>
<span data-ttu-id="f675b-127">指定資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f675b-127">Specifies the name of the server for the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f675b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f675b-128">-Confirm</span></span>
<span data-ttu-id="f675b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f675b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f675b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f675b-130">-WhatIf</span></span>
<span data-ttu-id="f675b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f675b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f675b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f675b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f675b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f675b-133">CommonParameters</span></span>
<span data-ttu-id="f675b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f675b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f675b-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f675b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f675b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f675b-136">INPUTS</span></span>

### <span data-ttu-id="f675b-137">所有</span><span class="sxs-lookup"><span data-stu-id="f675b-137">None</span></span>
<span data-ttu-id="f675b-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f675b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f675b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f675b-139">OUTPUTS</span></span>

### <span data-ttu-id="f675b-140">AzureSqlDatabaseAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="f675b-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="f675b-141">這個 Cmdlet 會傳回 **AzureSqlDatabaseAdvisorModel** 物件。</span><span class="sxs-lookup"><span data-stu-id="f675b-141">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="f675b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f675b-142">NOTES</span></span>

## <span data-ttu-id="f675b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f675b-143">RELATED LINKS</span></span>

[<span data-ttu-id="f675b-144">AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="f675b-144">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="f675b-145">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f675b-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

