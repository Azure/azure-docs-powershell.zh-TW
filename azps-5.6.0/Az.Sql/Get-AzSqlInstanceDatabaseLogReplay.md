---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7f2589c665bd24fdb2d017cd8cfd4ca055e3e429
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914318"
---
# <span data-ttu-id="0213d-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="0213d-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="0213d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0213d-102">SYNOPSIS</span></span>
<span data-ttu-id="0213d-103">獲得記錄重播服務狀態。</span><span class="sxs-lookup"><span data-stu-id="0213d-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="0213d-104">語法</span><span class="sxs-lookup"><span data-stu-id="0213d-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0213d-105">描述</span><span class="sxs-lookup"><span data-stu-id="0213d-105">DESCRIPTION</span></span>
<span data-ttu-id="0213d-106">**Get-AzSqlInstanceDatabaseLogReplay** Cmdlet 會取得給定資料庫的記錄重播服務狀態。</span><span class="sxs-lookup"><span data-stu-id="0213d-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="0213d-107">例子</span><span class="sxs-lookup"><span data-stu-id="0213d-107">EXAMPLES</span></span>

### <span data-ttu-id="0213d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0213d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="0213d-109">此命令將取得給定資料庫上的記錄重播服務狀態。</span><span class="sxs-lookup"><span data-stu-id="0213d-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="0213d-110">參數</span><span class="sxs-lookup"><span data-stu-id="0213d-110">PARAMETERS</span></span>

### <span data-ttu-id="0213d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0213d-111">-DefaultProfile</span></span>
<span data-ttu-id="0213d-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0213d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0213d-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0213d-113">-InstanceName</span></span>
<span data-ttu-id="0213d-114">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0213d-114">The name of the instance.</span></span>

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

### <span data-ttu-id="0213d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0213d-115">-Name</span></span>
<span data-ttu-id="0213d-116">要取取的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0213d-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="0213d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0213d-117">-ResourceGroupName</span></span>
<span data-ttu-id="0213d-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0213d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="0213d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0213d-119">CommonParameters</span></span>
<span data-ttu-id="0213d-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0213d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0213d-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0213d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0213d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0213d-122">INPUTS</span></span>

### <span data-ttu-id="0213d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0213d-123">System.String</span></span>

## <span data-ttu-id="0213d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0213d-124">OUTPUTS</span></span>

### <span data-ttu-id="0213d-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="0213d-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="0213d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0213d-126">NOTES</span></span>

## <span data-ttu-id="0213d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0213d-127">RELATED LINKS</span></span>
