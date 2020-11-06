---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450776"
---
# <span data-ttu-id="d787a-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d787a-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d787a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d787a-102">SYNOPSIS</span></span>
<span data-ttu-id="d787a-103">更新 Azure SQL Server Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="d787a-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d787a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d787a-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d787a-105">說明</span><span class="sxs-lookup"><span data-stu-id="d787a-105">DESCRIPTION</span></span>
<span data-ttu-id="d787a-106">**AzureRmSqlServerAdvisorAutoExecuteStatus** Cmdlet 會設定 Azure SQL Server Advisor 的自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="d787a-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="d787a-107">示例</span><span class="sxs-lookup"><span data-stu-id="d787a-107">EXAMPLES</span></span>

### <span data-ttu-id="d787a-108">範例1：啟用 Advisor 的自動執行</span><span class="sxs-lookup"><span data-stu-id="d787a-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="d787a-109">這個命令可啟用名為 CreateIndex 的 Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="d787a-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="d787a-110">參數</span><span class="sxs-lookup"><span data-stu-id="d787a-110">PARAMETERS</span></span>

### <span data-ttu-id="d787a-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="d787a-111">-AdvisorName</span></span>
<span data-ttu-id="d787a-112">指定此 Cmdlet 更新自動執行狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="d787a-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d787a-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d787a-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="d787a-114">指定此 Cmdlet 更新自動執行狀態的值。</span><span class="sxs-lookup"><span data-stu-id="d787a-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="d787a-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d787a-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d787a-116">後</span><span class="sxs-lookup"><span data-stu-id="d787a-116">Enabled</span></span>
- <span data-ttu-id="d787a-117">禁止</span><span class="sxs-lookup"><span data-stu-id="d787a-117">Disabled</span></span>
- <span data-ttu-id="d787a-118">設置</span><span class="sxs-lookup"><span data-stu-id="d787a-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d787a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d787a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d787a-120">指定伺服器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d787a-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="d787a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d787a-121">-ServerName</span></span>
<span data-ttu-id="d787a-122">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d787a-122">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d787a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="d787a-123">-Confirm</span></span>
<span data-ttu-id="d787a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d787a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d787a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d787a-125">-WhatIf</span></span>
<span data-ttu-id="d787a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d787a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d787a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d787a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d787a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d787a-128">-DefaultProfile</span></span>
<span data-ttu-id="d787a-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d787a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d787a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d787a-130">CommonParameters</span></span>
<span data-ttu-id="d787a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d787a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d787a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d787a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d787a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d787a-133">INPUTS</span></span>

## <span data-ttu-id="d787a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d787a-134">OUTPUTS</span></span>

### <span data-ttu-id="d787a-135">AzureSqlServerAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="d787a-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="d787a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d787a-136">NOTES</span></span>
* <span data-ttu-id="d787a-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，server，mssql，advisor</span><span class="sxs-lookup"><span data-stu-id="d787a-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="d787a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d787a-138">RELATED LINKS</span></span>

[<span data-ttu-id="d787a-139">AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="d787a-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="d787a-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d787a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
