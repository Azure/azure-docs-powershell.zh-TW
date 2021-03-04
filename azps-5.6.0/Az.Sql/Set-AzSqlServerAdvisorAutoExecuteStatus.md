---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: a80656e0a85401c4a98b62823b2b19ec2294d2f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917542"
---
# <span data-ttu-id="26976-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="26976-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="26976-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26976-102">SYNOPSIS</span></span>
<span data-ttu-id="26976-103">更新 Azure SQL Server Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="26976-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="26976-104">語法</span><span class="sxs-lookup"><span data-stu-id="26976-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26976-105">描述</span><span class="sxs-lookup"><span data-stu-id="26976-105">DESCRIPTION</span></span>
<span data-ttu-id="26976-106">**Set-AzSqlServerAdvisorAutoExecuteStatus** Cmdlet 會設定 Azure SQL Server Advisor 的自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="26976-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="26976-107">例子</span><span class="sxs-lookup"><span data-stu-id="26976-107">EXAMPLES</span></span>

### <span data-ttu-id="26976-108">範例 1：為顧問啟用自動執行</span><span class="sxs-lookup"><span data-stu-id="26976-108">Example 1: Enable auto execute for an Advisor</span></span>
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

<span data-ttu-id="26976-109">此命令會啟用名為 CreateIndex 的顧問自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="26976-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="26976-110">參數</span><span class="sxs-lookup"><span data-stu-id="26976-110">PARAMETERS</span></span>

### <span data-ttu-id="26976-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="26976-111">-AdvisorName</span></span>
<span data-ttu-id="26976-112">指定此 Cmdlet 更新自動執行狀態之建議程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="26976-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="26976-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="26976-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="26976-114">指定此 Cmdlet 更新自動執行狀態的值。</span><span class="sxs-lookup"><span data-stu-id="26976-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="26976-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="26976-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26976-116">啟用</span><span class="sxs-lookup"><span data-stu-id="26976-116">Enabled</span></span>
- <span data-ttu-id="26976-117">禁用</span><span class="sxs-lookup"><span data-stu-id="26976-117">Disabled</span></span>
- <span data-ttu-id="26976-118">預設</span><span class="sxs-lookup"><span data-stu-id="26976-118">Default</span></span>

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

### <span data-ttu-id="26976-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26976-119">-DefaultProfile</span></span>
<span data-ttu-id="26976-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="26976-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26976-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26976-121">-ResourceGroupName</span></span>
<span data-ttu-id="26976-122">指定伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="26976-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="26976-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26976-123">-ServerName</span></span>
<span data-ttu-id="26976-124">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="26976-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="26976-125">-確認</span><span class="sxs-lookup"><span data-stu-id="26976-125">-Confirm</span></span>
<span data-ttu-id="26976-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="26976-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26976-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26976-127">-WhatIf</span></span>
<span data-ttu-id="26976-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26976-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26976-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26976-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26976-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26976-130">CommonParameters</span></span>
<span data-ttu-id="26976-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26976-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26976-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26976-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26976-133">輸入</span><span class="sxs-lookup"><span data-stu-id="26976-133">INPUTS</span></span>

### <span data-ttu-id="26976-134">System.String</span><span class="sxs-lookup"><span data-stu-id="26976-134">System.String</span></span>

### <span data-ttu-id="26976-135">Microsoft.Azure.Commands.sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="26976-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="26976-136">輸出</span><span class="sxs-lookup"><span data-stu-id="26976-136">OUTPUTS</span></span>

### <span data-ttu-id="26976-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="26976-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="26976-138">筆記</span><span class="sxs-lookup"><span data-stu-id="26976-138">NOTES</span></span>
* <span data-ttu-id="26976-139">關鍵字：azure、azurerm、arm、resource、management、manager、sql、server、mssql、advisor</span><span class="sxs-lookup"><span data-stu-id="26976-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="26976-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="26976-140">RELATED LINKS</span></span>

[<span data-ttu-id="26976-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="26976-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="26976-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="26976-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
