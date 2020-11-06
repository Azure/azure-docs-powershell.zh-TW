---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450465"
---
# <span data-ttu-id="08f9a-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08f9a-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="08f9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="08f9a-103">取得資料庫的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="08f9a-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08f9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="08f9a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08f9a-105">說明</span><span class="sxs-lookup"><span data-stu-id="08f9a-105">DESCRIPTION</span></span>
<span data-ttu-id="08f9a-106">**AzureRmSqlDatabaseThreatDetectionPolicy** Cmdlet 會取得 Azure SQL 資料庫的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="08f9a-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="08f9a-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 、 *ServerName* 和 *DatabaseName* 參數來識別這個 Cmdlet 取得原則的資料庫。</span><span class="sxs-lookup"><span data-stu-id="08f9a-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="08f9a-108">示例</span><span class="sxs-lookup"><span data-stu-id="08f9a-108">EXAMPLES</span></span>

### <span data-ttu-id="08f9a-109">範例1：取得資料庫的威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="08f9a-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="08f9a-110">這個命令會取得名為 Database01 的資料庫的威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="08f9a-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="08f9a-111">資料庫位於名為 Server01 的伺服器上，該伺服器已指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="08f9a-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="08f9a-112">參數</span><span class="sxs-lookup"><span data-stu-id="08f9a-112">PARAMETERS</span></span>

### <span data-ttu-id="08f9a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08f9a-113">-DatabaseName</span></span>
<span data-ttu-id="08f9a-114">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="08f9a-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="08f9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f9a-115">-DefaultProfile</span></span>
<span data-ttu-id="08f9a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="08f9a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08f9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="08f9a-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08f9a-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="08f9a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08f9a-119">-ServerName</span></span>
<span data-ttu-id="08f9a-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="08f9a-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="08f9a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="08f9a-121">-Confirm</span></span>
<span data-ttu-id="08f9a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08f9a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f9a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f9a-123">-WhatIf</span></span>
<span data-ttu-id="08f9a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08f9a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f9a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08f9a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f9a-126">CommonParameters</span></span>
<span data-ttu-id="08f9a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08f9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f9a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08f9a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f9a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="08f9a-129">INPUTS</span></span>

###  
<span data-ttu-id="08f9a-130">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08f9a-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="08f9a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="08f9a-131">OUTPUTS</span></span>

### <span data-ttu-id="08f9a-132">DatabaseThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="08f9a-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="08f9a-133">這個 Cmdlet 會傳回 **DatabaseThreatDetectionPolicyModel** 物件。</span><span class="sxs-lookup"><span data-stu-id="08f9a-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="08f9a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="08f9a-134">NOTES</span></span>

## <span data-ttu-id="08f9a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="08f9a-135">RELATED LINKS</span></span>

[<span data-ttu-id="08f9a-136">移除-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08f9a-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



