---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 8e0c13565641a6033a22545d95af28df1c14a772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447612"
---
# <span data-ttu-id="36c0d-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="36c0d-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="36c0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="36c0d-103">從資料庫中移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="36c0d-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36c0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="36c0d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36c0d-105">說明</span><span class="sxs-lookup"><span data-stu-id="36c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="36c0d-106">**AzureRmSqlDatabaseThreatDetectionPolicy** Cmdlet 會從 AzureAzure SQL 資料庫中移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="36c0d-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="36c0d-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數來識別這個 Cmdlet 從中移除原則的資料庫。</span><span class="sxs-lookup"><span data-stu-id="36c0d-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="36c0d-108">示例</span><span class="sxs-lookup"><span data-stu-id="36c0d-108">EXAMPLES</span></span>

### <span data-ttu-id="36c0d-109">範例1：移除資料庫的威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="36c0d-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="36c0d-110">這個命令會從名為 Server01 的伺服器上名為 Database01 的資料庫中移除威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="36c0d-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="36c0d-111">參數</span><span class="sxs-lookup"><span data-stu-id="36c0d-111">PARAMETERS</span></span>

### <span data-ttu-id="36c0d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36c0d-112">-DatabaseName</span></span>
<span data-ttu-id="36c0d-113">指定應該移除威脅偵測原則的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="36c0d-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="36c0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c0d-114">-DefaultProfile</span></span>
<span data-ttu-id="36c0d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="36c0d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36c0d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36c0d-116">-PassThru</span></span>
<span data-ttu-id="36c0d-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="36c0d-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36c0d-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="36c0d-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c0d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c0d-119">-ResourceGroupName</span></span>
<span data-ttu-id="36c0d-120">指定伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36c0d-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="36c0d-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36c0d-121">-ServerName</span></span>
<span data-ttu-id="36c0d-122">指定資料庫在其上執行的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="36c0d-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="36c0d-123">-確認</span><span class="sxs-lookup"><span data-stu-id="36c0d-123">-Confirm</span></span>
<span data-ttu-id="36c0d-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36c0d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36c0d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c0d-125">-WhatIf</span></span>
<span data-ttu-id="36c0d-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36c0d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36c0d-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36c0d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36c0d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c0d-128">CommonParameters</span></span>
<span data-ttu-id="36c0d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36c0d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c0d-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36c0d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c0d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="36c0d-131">INPUTS</span></span>

###  
<span data-ttu-id="36c0d-132">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36c0d-132">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="36c0d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="36c0d-133">OUTPUTS</span></span>

### <span data-ttu-id="36c0d-134">DatabaseThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="36c0d-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="36c0d-135">這個 Cmdlet 會傳回 **DatabaseThreatDetectionPolicyModel** 物件。</span><span class="sxs-lookup"><span data-stu-id="36c0d-135">This cmdlet returns a **DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="36c0d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="36c0d-136">NOTES</span></span>

## <span data-ttu-id="36c0d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="36c0d-137">RELATED LINKS</span></span>

[<span data-ttu-id="36c0d-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="36c0d-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


