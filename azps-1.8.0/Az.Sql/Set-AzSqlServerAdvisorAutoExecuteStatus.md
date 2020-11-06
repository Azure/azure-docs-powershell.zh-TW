---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa3aff9a1e471445c49cbfb23b5799a97c54025d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614701"
---
# <span data-ttu-id="64fb1-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="64fb1-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="64fb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="64fb1-103">更新 Azure SQL Server Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="64fb1-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="64fb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="64fb1-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64fb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="64fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="64fb1-106">**AzSqlServerAdvisorAutoExecuteStatus** Cmdlet 會設定 Azure SQL Server Advisor 的自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="64fb1-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="64fb1-107">示例</span><span class="sxs-lookup"><span data-stu-id="64fb1-107">EXAMPLES</span></span>

### <span data-ttu-id="64fb1-108">範例1：啟用 Advisor 的自動執行</span><span class="sxs-lookup"><span data-stu-id="64fb1-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="64fb1-109">這個命令可啟用名為 CreateIndex 的 Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="64fb1-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="64fb1-110">參數</span><span class="sxs-lookup"><span data-stu-id="64fb1-110">PARAMETERS</span></span>

### <span data-ttu-id="64fb1-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="64fb1-111">-AdvisorName</span></span>
<span data-ttu-id="64fb1-112">指定此 Cmdlet 更新自動執行狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="64fb1-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="64fb1-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="64fb1-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="64fb1-114">指定此 Cmdlet 更新自動執行狀態的值。</span><span class="sxs-lookup"><span data-stu-id="64fb1-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="64fb1-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="64fb1-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64fb1-116">後</span><span class="sxs-lookup"><span data-stu-id="64fb1-116">Enabled</span></span>
- <span data-ttu-id="64fb1-117">禁止</span><span class="sxs-lookup"><span data-stu-id="64fb1-117">Disabled</span></span>
- <span data-ttu-id="64fb1-118">設置</span><span class="sxs-lookup"><span data-stu-id="64fb1-118">Default</span></span>

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

### <span data-ttu-id="64fb1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64fb1-119">-DefaultProfile</span></span>
<span data-ttu-id="64fb1-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="64fb1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64fb1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64fb1-121">-ResourceGroupName</span></span>
<span data-ttu-id="64fb1-122">指定伺服器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64fb1-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="64fb1-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="64fb1-123">-ServerName</span></span>
<span data-ttu-id="64fb1-124">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="64fb1-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="64fb1-125">-確認</span><span class="sxs-lookup"><span data-stu-id="64fb1-125">-Confirm</span></span>
<span data-ttu-id="64fb1-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64fb1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64fb1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64fb1-127">-WhatIf</span></span>
<span data-ttu-id="64fb1-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64fb1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64fb1-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64fb1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64fb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64fb1-130">CommonParameters</span></span>
<span data-ttu-id="64fb1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64fb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64fb1-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64fb1-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64fb1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="64fb1-133">INPUTS</span></span>

### <span data-ttu-id="64fb1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="64fb1-134">System.String</span></span>

### <span data-ttu-id="64fb1-135">AdvisorAutoExecuteStatus 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="64fb1-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="64fb1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="64fb1-136">OUTPUTS</span></span>

### <span data-ttu-id="64fb1-137">AzureSqlServerAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="64fb1-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="64fb1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="64fb1-138">NOTES</span></span>
* <span data-ttu-id="64fb1-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，server，mssql，advisor</span><span class="sxs-lookup"><span data-stu-id="64fb1-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="64fb1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="64fb1-140">RELATED LINKS</span></span>

[<span data-ttu-id="64fb1-141">AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="64fb1-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="64fb1-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="64fb1-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)