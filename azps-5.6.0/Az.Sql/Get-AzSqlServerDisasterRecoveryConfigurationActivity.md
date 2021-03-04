---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 68e81a7f51ca385d5671698ad8624f523ae98c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904578"
---
# <span data-ttu-id="c970b-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="c970b-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="c970b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c970b-102">SYNOPSIS</span></span>
<span data-ttu-id="c970b-103">為資料庫伺服器系統復原組進行活動。</span><span class="sxs-lookup"><span data-stu-id="c970b-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="c970b-104">語法</span><span class="sxs-lookup"><span data-stu-id="c970b-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c970b-105">描述</span><span class="sxs-lookup"><span data-stu-id="c970b-105">DESCRIPTION</span></span>
<span data-ttu-id="c970b-106">**Get-AzSqlServerDsterRecoveryConfigurationActivity** Cmdlet 會取得 SQL 資料庫伺服器系統復原組式的活動。</span><span class="sxs-lookup"><span data-stu-id="c970b-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="c970b-107">例子</span><span class="sxs-lookup"><span data-stu-id="c970b-107">EXAMPLES</span></span>

## <span data-ttu-id="c970b-108">參數</span><span class="sxs-lookup"><span data-stu-id="c970b-108">PARAMETERS</span></span>

### <span data-ttu-id="c970b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c970b-109">-DefaultProfile</span></span>
<span data-ttu-id="c970b-110">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c970b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c970b-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c970b-111">-OperationId</span></span>
<span data-ttu-id="c970b-112">指定作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="c970b-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c970b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c970b-113">-ResourceGroupName</span></span>
<span data-ttu-id="c970b-114">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c970b-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c970b-115">-ServerD星號RecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c970b-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="c970b-116">指定伺服器系統復原群組原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c970b-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="c970b-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c970b-117">-ServerName</span></span>
<span data-ttu-id="c970b-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c970b-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c970b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c970b-119">-Confirm</span></span>
<span data-ttu-id="c970b-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c970b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c970b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c970b-121">-WhatIf</span></span>
<span data-ttu-id="c970b-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c970b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c970b-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c970b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c970b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c970b-124">CommonParameters</span></span>
<span data-ttu-id="c970b-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c970b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c970b-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c970b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c970b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c970b-127">INPUTS</span></span>

### <span data-ttu-id="c970b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c970b-128">System.String</span></span>

### <span data-ttu-id="c970b-129">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c970b-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c970b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c970b-130">OUTPUTS</span></span>

### <span data-ttu-id="c970b-131">Microsoft.Azure.Commands.Sql.ServerDazsterRecoveryConfiguration.Model.AzureSqlServerDsterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="c970b-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="c970b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c970b-132">NOTES</span></span>

## <span data-ttu-id="c970b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c970b-133">RELATED LINKS</span></span>

[<span data-ttu-id="c970b-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c970b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
