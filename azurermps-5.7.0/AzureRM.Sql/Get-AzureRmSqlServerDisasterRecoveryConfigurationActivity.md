---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 3c67c432f8f49927af4cbf357a4338f528c826b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453991"
---
# <span data-ttu-id="2889e-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="2889e-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="2889e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2889e-102">SYNOPSIS</span></span>
<span data-ttu-id="2889e-103">取得資料庫伺服器系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="2889e-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2889e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2889e-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2889e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2889e-105">DESCRIPTION</span></span>
<span data-ttu-id="2889e-106">**AzureRmSqlServerDisasterRecoveryConfigurationActivity** Cmdlet 會取得 SQL database server 系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="2889e-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2889e-107">示例</span><span class="sxs-lookup"><span data-stu-id="2889e-107">EXAMPLES</span></span>

## <span data-ttu-id="2889e-108">參數</span><span class="sxs-lookup"><span data-stu-id="2889e-108">PARAMETERS</span></span>

### <span data-ttu-id="2889e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2889e-109">-DefaultProfile</span></span>
<span data-ttu-id="2889e-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2889e-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2889e-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2889e-111">-OperationId</span></span>
<span data-ttu-id="2889e-112">指定操作 ID。</span><span class="sxs-lookup"><span data-stu-id="2889e-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="2889e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2889e-113">-ResourceGroupName</span></span>
<span data-ttu-id="2889e-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2889e-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2889e-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2889e-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="2889e-116">指定伺服器系統的復原配置名稱。</span><span class="sxs-lookup"><span data-stu-id="2889e-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="2889e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2889e-117">-ServerName</span></span>
<span data-ttu-id="2889e-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2889e-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2889e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2889e-119">-Confirm</span></span>
<span data-ttu-id="2889e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2889e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2889e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2889e-121">-WhatIf</span></span>
<span data-ttu-id="2889e-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2889e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2889e-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2889e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2889e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2889e-124">CommonParameters</span></span>
<span data-ttu-id="2889e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2889e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2889e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2889e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2889e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2889e-127">INPUTS</span></span>

### <span data-ttu-id="2889e-128">所有</span><span class="sxs-lookup"><span data-stu-id="2889e-128">None</span></span>
<span data-ttu-id="2889e-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2889e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2889e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2889e-130">OUTPUTS</span></span>

## <span data-ttu-id="2889e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2889e-131">NOTES</span></span>

## <span data-ttu-id="2889e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2889e-132">RELATED LINKS</span></span>

[<span data-ttu-id="2889e-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="2889e-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
