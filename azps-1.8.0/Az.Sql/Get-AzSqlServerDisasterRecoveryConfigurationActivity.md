---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 8fcd9b165722d1328bfbc87dd906f8b86e456579
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620389"
---
# <span data-ttu-id="80207-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="80207-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="80207-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80207-102">SYNOPSIS</span></span>
<span data-ttu-id="80207-103">取得資料庫伺服器系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="80207-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="80207-104">句法</span><span class="sxs-lookup"><span data-stu-id="80207-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80207-105">說明</span><span class="sxs-lookup"><span data-stu-id="80207-105">DESCRIPTION</span></span>
<span data-ttu-id="80207-106">**AzSqlServerDisasterRecoveryConfigurationActivity** Cmdlet 會取得 SQL database server 系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="80207-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="80207-107">示例</span><span class="sxs-lookup"><span data-stu-id="80207-107">EXAMPLES</span></span>

## <span data-ttu-id="80207-108">參數</span><span class="sxs-lookup"><span data-stu-id="80207-108">PARAMETERS</span></span>

### <span data-ttu-id="80207-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80207-109">-DefaultProfile</span></span>
<span data-ttu-id="80207-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="80207-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80207-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="80207-111">-OperationId</span></span>
<span data-ttu-id="80207-112">指定操作 ID。</span><span class="sxs-lookup"><span data-stu-id="80207-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="80207-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80207-113">-ResourceGroupName</span></span>
<span data-ttu-id="80207-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80207-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="80207-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="80207-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="80207-116">指定伺服器系統的復原配置名稱。</span><span class="sxs-lookup"><span data-stu-id="80207-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="80207-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80207-117">-ServerName</span></span>
<span data-ttu-id="80207-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="80207-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="80207-119">-確認</span><span class="sxs-lookup"><span data-stu-id="80207-119">-Confirm</span></span>
<span data-ttu-id="80207-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80207-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80207-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80207-121">-WhatIf</span></span>
<span data-ttu-id="80207-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80207-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80207-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80207-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80207-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80207-124">CommonParameters</span></span>
<span data-ttu-id="80207-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80207-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80207-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="80207-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80207-127">輸入</span><span class="sxs-lookup"><span data-stu-id="80207-127">INPUTS</span></span>

### <span data-ttu-id="80207-128">System.object</span><span class="sxs-lookup"><span data-stu-id="80207-128">System.String</span></span>

### <span data-ttu-id="80207-129">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80207-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="80207-130">輸出</span><span class="sxs-lookup"><span data-stu-id="80207-130">OUTPUTS</span></span>

### <span data-ttu-id="80207-131">AzureSqlServerDisasterRecoveryConfigurationActivityModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="80207-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="80207-132">筆記</span><span class="sxs-lookup"><span data-stu-id="80207-132">NOTES</span></span>

## <span data-ttu-id="80207-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="80207-133">RELATED LINKS</span></span>

[<span data-ttu-id="80207-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="80207-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)