---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: f5e7455a253c86fe363b72c5d4c0e8ff47b96f56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624872"
---
# <span data-ttu-id="f1423-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f1423-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="f1423-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1423-102">SYNOPSIS</span></span>
<span data-ttu-id="f1423-103">取得彈性池中作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f1423-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1423-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1423-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1423-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1423-105">DESCRIPTION</span></span>
<span data-ttu-id="f1423-106">**AzureRmSqlElasticPoolActivity** Cmdlet 會取得 Azure SQL 資料庫彈性池中作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f1423-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="f1423-107">您可以查看 [建立池] 與 [配置更新] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="f1423-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="f1423-108">示例</span><span class="sxs-lookup"><span data-stu-id="f1423-108">EXAMPLES</span></span>

### <span data-ttu-id="f1423-109">範例1：取得彈性池作業的狀態</span><span class="sxs-lookup"><span data-stu-id="f1423-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f1423-110">這個命令會取得名為 ElasticPool01 的彈性池作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f1423-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="f1423-111">參數</span><span class="sxs-lookup"><span data-stu-id="f1423-111">PARAMETERS</span></span>

### <span data-ttu-id="f1423-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1423-112">-DefaultProfile</span></span>
<span data-ttu-id="f1423-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f1423-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1423-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f1423-114">-ElasticPoolName</span></span>
<span data-ttu-id="f1423-115">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1423-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="f1423-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f1423-116">-OperationId</span></span>
<span data-ttu-id="f1423-117">要檢索的操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1423-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="f1423-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1423-118">-ResourceGroupName</span></span>
<span data-ttu-id="f1423-119">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1423-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f1423-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1423-120">-ServerName</span></span>
<span data-ttu-id="f1423-121">指定包含彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f1423-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="f1423-122">-確認</span><span class="sxs-lookup"><span data-stu-id="f1423-122">-Confirm</span></span>
<span data-ttu-id="f1423-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1423-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1423-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1423-124">-WhatIf</span></span>
<span data-ttu-id="f1423-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1423-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1423-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1423-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1423-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1423-127">CommonParameters</span></span>
<span data-ttu-id="f1423-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1423-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1423-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1423-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1423-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f1423-130">INPUTS</span></span>

### <span data-ttu-id="f1423-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f1423-131">System.String</span></span>

### <span data-ttu-id="f1423-132">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f1423-132">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f1423-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f1423-133">OUTPUTS</span></span>

### <span data-ttu-id="f1423-134">AzureSqlElasticPoolActivityModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="f1423-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="f1423-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f1423-135">NOTES</span></span>

## <span data-ttu-id="f1423-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1423-136">RELATED LINKS</span></span>

[<span data-ttu-id="f1423-137">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1423-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f1423-138">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f1423-138">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="f1423-139">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1423-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f1423-140">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1423-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f1423-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1423-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


