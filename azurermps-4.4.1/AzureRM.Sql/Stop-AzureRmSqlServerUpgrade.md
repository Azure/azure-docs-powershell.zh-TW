---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c9940f5278390fc72dbd8e7d906718f01375583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625653"
---
# <span data-ttu-id="e212d-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="e212d-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="e212d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e212d-102">SYNOPSIS</span></span>
<span data-ttu-id="e212d-103">停止升級 SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="e212d-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e212d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e212d-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e212d-105">說明</span><span class="sxs-lookup"><span data-stu-id="e212d-105">DESCRIPTION</span></span>
<span data-ttu-id="e212d-106">**Stop-AzureRmSqlServerUpgrade** Cmdlet 會停止升級 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="e212d-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="e212d-107">示例</span><span class="sxs-lookup"><span data-stu-id="e212d-107">EXAMPLES</span></span>

### <span data-ttu-id="e212d-108">範例1：停止伺服器升級</span><span class="sxs-lookup"><span data-stu-id="e212d-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="e212d-109">這個命令會停止要求，以升級指派給名為 ResourceGroup01 之資源群組的伺服器（名為 Server02）。</span><span class="sxs-lookup"><span data-stu-id="e212d-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e212d-110">參數</span><span class="sxs-lookup"><span data-stu-id="e212d-110">PARAMETERS</span></span>

### <span data-ttu-id="e212d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e212d-111">-Force</span></span>
<span data-ttu-id="e212d-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e212d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e212d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e212d-113">-ResourceGroupName</span></span>
<span data-ttu-id="e212d-114">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e212d-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e212d-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e212d-115">-ServerName</span></span>
<span data-ttu-id="e212d-116">指定此 Cmdlet 停止升級之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e212d-116">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="e212d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e212d-117">-Confirm</span></span>
<span data-ttu-id="e212d-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e212d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e212d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e212d-119">-WhatIf</span></span>
<span data-ttu-id="e212d-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e212d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e212d-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e212d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e212d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e212d-122">-DefaultProfile</span></span>
<span data-ttu-id="e212d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e212d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e212d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e212d-124">CommonParameters</span></span>
<span data-ttu-id="e212d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e212d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e212d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e212d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e212d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e212d-127">INPUTS</span></span>

### <span data-ttu-id="e212d-128">AzureSqlServerUpgradeModel 中的 [ServerUpgrade]</span><span class="sxs-lookup"><span data-stu-id="e212d-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="e212d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e212d-129">OUTPUTS</span></span>

## <span data-ttu-id="e212d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e212d-130">NOTES</span></span>

## <span data-ttu-id="e212d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e212d-131">RELATED LINKS</span></span>

[<span data-ttu-id="e212d-132">AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="e212d-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="e212d-133">開始-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="e212d-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="e212d-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e212d-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


