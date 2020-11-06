---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d2a92e7209745873364b5de114916bc48b0a3b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446646"
---
# <span data-ttu-id="d4eed-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="d4eed-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="d4eed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4eed-102">SYNOPSIS</span></span>
<span data-ttu-id="d4eed-103">取得 Azure SQL 資料庫伺服器升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4eed-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4eed-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4eed-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4eed-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4eed-105">DESCRIPTION</span></span>
<span data-ttu-id="d4eed-106">**AzureRmSqlServerUpgrade** Cmdlet 會取得 Azure SQL 資料庫伺服器升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4eed-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="d4eed-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4eed-107">EXAMPLES</span></span>

### <span data-ttu-id="d4eed-108">範例1：取得升級狀態</span><span class="sxs-lookup"><span data-stu-id="d4eed-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="d4eed-109">這個命令會在名為 ResourceGroup01 的資源群組中，從名為 Server01 的伺服器中取得升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4eed-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d4eed-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4eed-110">PARAMETERS</span></span>

### <span data-ttu-id="d4eed-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4eed-111">-ResourceGroupName</span></span>
<span data-ttu-id="d4eed-112">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4eed-112">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d4eed-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d4eed-113">-ServerName</span></span>
<span data-ttu-id="d4eed-114">指定此 Cmdlet 取得升級狀態的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d4eed-114">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="d4eed-115">-確認</span><span class="sxs-lookup"><span data-stu-id="d4eed-115">-Confirm</span></span>
<span data-ttu-id="d4eed-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4eed-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4eed-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4eed-117">-WhatIf</span></span>
<span data-ttu-id="d4eed-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4eed-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4eed-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4eed-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4eed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4eed-120">-DefaultProfile</span></span>
<span data-ttu-id="d4eed-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4eed-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4eed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4eed-122">CommonParameters</span></span>
<span data-ttu-id="d4eed-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4eed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4eed-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4eed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4eed-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d4eed-125">INPUTS</span></span>

## <span data-ttu-id="d4eed-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d4eed-126">OUTPUTS</span></span>

### <span data-ttu-id="d4eed-127">AzureSqlServerUpgradeModel 中的 [ServerUpgrade]</span><span class="sxs-lookup"><span data-stu-id="d4eed-127">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="d4eed-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d4eed-128">NOTES</span></span>

## <span data-ttu-id="d4eed-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4eed-129">RELATED LINKS</span></span>

[<span data-ttu-id="d4eed-130">開始-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="d4eed-130">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="d4eed-131">停止 AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="d4eed-131">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="d4eed-132">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d4eed-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


