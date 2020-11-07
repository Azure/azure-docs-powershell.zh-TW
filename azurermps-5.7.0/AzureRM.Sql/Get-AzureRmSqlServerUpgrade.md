---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c1be584b1110f720d1d5d50b32d7efa5d8586db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625397"
---
# <span data-ttu-id="d66f7-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="d66f7-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="d66f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d66f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d66f7-103">取得 Azure SQL 資料庫伺服器升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="d66f7-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d66f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d66f7-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d66f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="d66f7-105">DESCRIPTION</span></span>
<span data-ttu-id="d66f7-106">**AzureRmSqlServerUpgrade** Cmdlet 會取得 Azure SQL 資料庫伺服器升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="d66f7-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="d66f7-107">示例</span><span class="sxs-lookup"><span data-stu-id="d66f7-107">EXAMPLES</span></span>

### <span data-ttu-id="d66f7-108">範例1：取得升級狀態</span><span class="sxs-lookup"><span data-stu-id="d66f7-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="d66f7-109">這個命令會在名為 ResourceGroup01 的資源群組中，從名為 Server01 的伺服器中取得升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="d66f7-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d66f7-110">參數</span><span class="sxs-lookup"><span data-stu-id="d66f7-110">PARAMETERS</span></span>

### <span data-ttu-id="d66f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66f7-111">-DefaultProfile</span></span>
<span data-ttu-id="d66f7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d66f7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d66f7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66f7-113">-ResourceGroupName</span></span>
<span data-ttu-id="d66f7-114">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d66f7-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d66f7-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d66f7-115">-ServerName</span></span>
<span data-ttu-id="d66f7-116">指定此 Cmdlet 取得升級狀態的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d66f7-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="d66f7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="d66f7-117">-Confirm</span></span>
<span data-ttu-id="d66f7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d66f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66f7-119">-WhatIf</span></span>
<span data-ttu-id="d66f7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d66f7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66f7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d66f7-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66f7-122">CommonParameters</span></span>
<span data-ttu-id="d66f7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d66f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66f7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d66f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66f7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d66f7-125">INPUTS</span></span>

### <span data-ttu-id="d66f7-126">所有</span><span class="sxs-lookup"><span data-stu-id="d66f7-126">None</span></span>
<span data-ttu-id="d66f7-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d66f7-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d66f7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d66f7-128">OUTPUTS</span></span>

### <span data-ttu-id="d66f7-129">AzureSqlServerUpgradeModel 中的 [ServerUpgrade]</span><span class="sxs-lookup"><span data-stu-id="d66f7-129">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="d66f7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d66f7-130">NOTES</span></span>

## <span data-ttu-id="d66f7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d66f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="d66f7-132">開始-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="d66f7-132">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="d66f7-133">停止 AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="d66f7-133">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="d66f7-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d66f7-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


