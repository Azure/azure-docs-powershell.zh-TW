---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437103"
---
# <span data-ttu-id="a2bd2-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="a2bd2-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="a2bd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2bd2-103">取得記錄重播服務狀態。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="a2bd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2bd2-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2bd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="a2bd2-106">**AzSqlInstanceDatabaseLogReplay** Cmdlet 會取得指定資料庫上的記錄重播服務狀態。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="a2bd2-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="a2bd2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a2bd2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="a2bd2-109">這個命令會在指定的資料庫上取得記錄重放服務狀態。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="a2bd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a2bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="a2bd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2bd2-111">-DefaultProfile</span></span>
<span data-ttu-id="a2bd2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2bd2-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a2bd2-113">-InstanceName</span></span>
<span data-ttu-id="a2bd2-114">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-114">The name of the instance.</span></span>

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

### <span data-ttu-id="a2bd2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2bd2-115">-Name</span></span>
<span data-ttu-id="a2bd2-116">要檢索之實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="a2bd2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2bd2-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2bd2-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2bd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2bd2-119">CommonParameters</span></span>
<span data-ttu-id="a2bd2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2bd2-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2bd2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2bd2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a2bd2-122">INPUTS</span></span>

### <span data-ttu-id="a2bd2-123">System.object</span><span class="sxs-lookup"><span data-stu-id="a2bd2-123">System.String</span></span>

## <span data-ttu-id="a2bd2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a2bd2-124">OUTPUTS</span></span>

### <span data-ttu-id="a2bd2-125">AzureSqlManagedDatabaseRestoreDetailsResultModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="a2bd2-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="a2bd2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a2bd2-126">NOTES</span></span>

## <span data-ttu-id="a2bd2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2bd2-127">RELATED LINKS</span></span>
