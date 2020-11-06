---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 0cabae7f7b803001a03b64eec027925733d05545
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453240"
---
# <span data-ttu-id="d5cb0-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="d5cb0-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="d5cb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cb0-103">取得資料庫伺服器系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5cb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5cb0-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5cb0-105">說明</span><span class="sxs-lookup"><span data-stu-id="d5cb0-105">DESCRIPTION</span></span>
<span data-ttu-id="d5cb0-106">**AzureRmSqlServerDisasterRecoveryConfigurationActivity** Cmdlet 會取得 SQL database server 系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d5cb0-107">示例</span><span class="sxs-lookup"><span data-stu-id="d5cb0-107">EXAMPLES</span></span>

## <span data-ttu-id="d5cb0-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5cb0-108">PARAMETERS</span></span>

### <span data-ttu-id="d5cb0-109">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d5cb0-109">-OperationId</span></span>
<span data-ttu-id="d5cb0-110">指定操作 ID。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-110">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="d5cb0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5cb0-111">-ResourceGroupName</span></span>
<span data-ttu-id="d5cb0-112">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d5cb0-113">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d5cb0-113">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="d5cb0-114">指定伺服器系統的復原配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-114">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="d5cb0-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5cb0-115">-ServerName</span></span>
<span data-ttu-id="d5cb0-116">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d5cb0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="d5cb0-117">-Confirm</span></span>
<span data-ttu-id="d5cb0-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5cb0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5cb0-119">-WhatIf</span></span>
<span data-ttu-id="d5cb0-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5cb0-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5cb0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5cb0-122">-DefaultProfile</span></span>
<span data-ttu-id="d5cb0-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5cb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cb0-124">CommonParameters</span></span>
<span data-ttu-id="d5cb0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cb0-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5cb0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cb0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d5cb0-127">INPUTS</span></span>

## <span data-ttu-id="d5cb0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d5cb0-128">OUTPUTS</span></span>

## <span data-ttu-id="d5cb0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d5cb0-129">NOTES</span></span>

## <span data-ttu-id="d5cb0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5cb0-130">RELATED LINKS</span></span>

[<span data-ttu-id="d5cb0-131">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d5cb0-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
