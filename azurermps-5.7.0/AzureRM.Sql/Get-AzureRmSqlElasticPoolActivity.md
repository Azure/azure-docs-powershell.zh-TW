---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 88052c9f47359e0080e193f5a2dbb1004b48b0e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624278"
---
# <span data-ttu-id="f24a1-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f24a1-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="f24a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f24a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f24a1-103">取得彈性池中作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f24a1-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f24a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f24a1-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f24a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f24a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f24a1-106">**AzureRmSqlElasticPoolActivity** Cmdlet 會取得 Azure SQL 資料庫彈性池中作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f24a1-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="f24a1-107">您可以查看 [建立池] 與 [配置更新] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="f24a1-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="f24a1-108">示例</span><span class="sxs-lookup"><span data-stu-id="f24a1-108">EXAMPLES</span></span>

### <span data-ttu-id="f24a1-109">範例1：取得彈性池作業的狀態</span><span class="sxs-lookup"><span data-stu-id="f24a1-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f24a1-110">這個命令會取得名為 ElasticPool01 的彈性池作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f24a1-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="f24a1-111">參數</span><span class="sxs-lookup"><span data-stu-id="f24a1-111">PARAMETERS</span></span>

### <span data-ttu-id="f24a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24a1-112">-DefaultProfile</span></span>
<span data-ttu-id="f24a1-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f24a1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f24a1-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f24a1-114">-ElasticPoolName</span></span>
<span data-ttu-id="f24a1-115">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="f24a1-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="f24a1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f24a1-116">-ResourceGroupName</span></span>
<span data-ttu-id="f24a1-117">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f24a1-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f24a1-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f24a1-118">-ServerName</span></span>
<span data-ttu-id="f24a1-119">指定包含彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f24a1-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="f24a1-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f24a1-120">-Confirm</span></span>
<span data-ttu-id="f24a1-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f24a1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24a1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24a1-122">-WhatIf</span></span>
<span data-ttu-id="f24a1-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f24a1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24a1-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f24a1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24a1-125">CommonParameters</span></span>
<span data-ttu-id="f24a1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f24a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24a1-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f24a1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24a1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f24a1-128">INPUTS</span></span>

### <span data-ttu-id="f24a1-129">所有</span><span class="sxs-lookup"><span data-stu-id="f24a1-129">None</span></span>
<span data-ttu-id="f24a1-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f24a1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f24a1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f24a1-131">OUTPUTS</span></span>

### <span data-ttu-id="f24a1-132">AzureSqlElasticPoolActivityModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="f24a1-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="f24a1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f24a1-133">NOTES</span></span>

## <span data-ttu-id="f24a1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f24a1-134">RELATED LINKS</span></span>

[<span data-ttu-id="f24a1-135">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f24a1-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f24a1-136">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f24a1-136">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="f24a1-137">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f24a1-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f24a1-138">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f24a1-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f24a1-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f24a1-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


