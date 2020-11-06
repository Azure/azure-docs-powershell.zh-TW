---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 87744454627feaadc8c953e1ad4e50016f14879f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452015"
---
# <span data-ttu-id="004d0-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="004d0-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="004d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="004d0-102">SYNOPSIS</span></span>
<span data-ttu-id="004d0-103">取消彈性池中的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="004d0-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="004d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="004d0-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="004d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="004d0-105">DESCRIPTION</span></span>
<span data-ttu-id="004d0-106">**AzureRmSqlElasticPoolActivity** Cmdlet 會取消彈性池中的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="004d0-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="004d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="004d0-107">EXAMPLES</span></span>

### <span data-ttu-id="004d0-108">範例1：取消彈性池中的非同步更新作業</span><span class="sxs-lookup"><span data-stu-id="004d0-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
```

<span data-ttu-id="004d0-109">這個命令會取消彈性池中的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="004d0-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="004d0-110">參數</span><span class="sxs-lookup"><span data-stu-id="004d0-110">PARAMETERS</span></span>

### <span data-ttu-id="004d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004d0-111">-DefaultProfile</span></span>
<span data-ttu-id="004d0-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="004d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="004d0-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="004d0-113">-ElasticPoolName</span></span>
<span data-ttu-id="004d0-114">Azure SQL 彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="004d0-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004d0-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="004d0-115">-OperationId</span></span>
<span data-ttu-id="004d0-116">要檢索的操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="004d0-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="004d0-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="004d0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="004d0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="004d0-119">-ServerName</span></span>
<span data-ttu-id="004d0-120">彈性池所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="004d0-120">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004d0-121">-確認</span><span class="sxs-lookup"><span data-stu-id="004d0-121">-Confirm</span></span>
<span data-ttu-id="004d0-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="004d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004d0-123">-WhatIf</span></span>
<span data-ttu-id="004d0-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="004d0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="004d0-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="004d0-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004d0-126">CommonParameters</span></span>
<span data-ttu-id="004d0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="004d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004d0-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="004d0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004d0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="004d0-129">INPUTS</span></span>

### <span data-ttu-id="004d0-130">所有</span><span class="sxs-lookup"><span data-stu-id="004d0-130">None</span></span>

<span data-ttu-id="004d0-131">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="004d0-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="004d0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="004d0-132">OUTPUTS</span></span>

### <span data-ttu-id="004d0-133">System.object</span><span class="sxs-lookup"><span data-stu-id="004d0-133">System.Object</span></span>

## <span data-ttu-id="004d0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="004d0-134">NOTES</span></span>

## <span data-ttu-id="004d0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="004d0-135">RELATED LINKS</span></span>



