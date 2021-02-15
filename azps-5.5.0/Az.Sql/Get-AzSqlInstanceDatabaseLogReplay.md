---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138298"
---
# <span data-ttu-id="14680-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="14680-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="14680-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14680-102">SYNOPSIS</span></span>
<span data-ttu-id="14680-103">取得記錄重播服務狀態。</span><span class="sxs-lookup"><span data-stu-id="14680-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="14680-104">句法</span><span class="sxs-lookup"><span data-stu-id="14680-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14680-105">說明</span><span class="sxs-lookup"><span data-stu-id="14680-105">DESCRIPTION</span></span>
<span data-ttu-id="14680-106">**AzSqlInstanceDatabaseLogReplay** Cmdlet 會取得指定資料庫上的記錄重播服務狀態。</span><span class="sxs-lookup"><span data-stu-id="14680-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="14680-107">示例</span><span class="sxs-lookup"><span data-stu-id="14680-107">EXAMPLES</span></span>

### <span data-ttu-id="14680-108">範例1</span><span class="sxs-lookup"><span data-stu-id="14680-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="14680-109">這個命令會在指定的資料庫上取得記錄重放服務狀態。</span><span class="sxs-lookup"><span data-stu-id="14680-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="14680-110">參數</span><span class="sxs-lookup"><span data-stu-id="14680-110">PARAMETERS</span></span>

### <span data-ttu-id="14680-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14680-111">-DefaultProfile</span></span>
<span data-ttu-id="14680-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14680-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14680-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="14680-113">-InstanceName</span></span>
<span data-ttu-id="14680-114">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="14680-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14680-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="14680-115">-Name</span></span>
<span data-ttu-id="14680-116">要檢索之實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="14680-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14680-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14680-117">-ResourceGroupName</span></span>
<span data-ttu-id="14680-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14680-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="14680-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14680-119">CommonParameters</span></span>
<span data-ttu-id="14680-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14680-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14680-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14680-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14680-122">輸入</span><span class="sxs-lookup"><span data-stu-id="14680-122">INPUTS</span></span>

### <span data-ttu-id="14680-123">System.object</span><span class="sxs-lookup"><span data-stu-id="14680-123">System.String</span></span>

## <span data-ttu-id="14680-124">輸出</span><span class="sxs-lookup"><span data-stu-id="14680-124">OUTPUTS</span></span>

### <span data-ttu-id="14680-125">AzureSqlManagedDatabaseRestoreDetailsResultModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="14680-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="14680-126">筆記</span><span class="sxs-lookup"><span data-stu-id="14680-126">NOTES</span></span>

## <span data-ttu-id="14680-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="14680-127">RELATED LINKS</span></span>
