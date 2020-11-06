---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447097"
---
# <span data-ttu-id="46d86-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="46d86-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="46d86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46d86-102">SYNOPSIS</span></span>
<span data-ttu-id="46d86-103">建立新的連線資訊物件，以指定連線的伺服器類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="46d86-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46d86-104">句法</span><span class="sxs-lookup"><span data-stu-id="46d86-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="46d86-105">說明</span><span class="sxs-lookup"><span data-stu-id="46d86-105">DESCRIPTION</span></span>
<span data-ttu-id="46d86-106">New-AzureRmDataMigrationConnectionInfo Cmdlet 會建立新的連接資訊物件，以指定連線的伺服器類型。</span><span class="sxs-lookup"><span data-stu-id="46d86-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="46d86-107">示例</span><span class="sxs-lookup"><span data-stu-id="46d86-107">EXAMPLES</span></span>

### <span data-ttu-id="46d86-108">範例1</span><span class="sxs-lookup"><span data-stu-id="46d86-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="46d86-109">前面的範例會建立新的連線資訊物件，提供 SQL 作為 ServerType 參數。</span><span class="sxs-lookup"><span data-stu-id="46d86-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="46d86-110">參數</span><span class="sxs-lookup"><span data-stu-id="46d86-110">PARAMETERS</span></span>

### <span data-ttu-id="46d86-111">-確認</span><span class="sxs-lookup"><span data-stu-id="46d86-111">-Confirm</span></span>
<span data-ttu-id="46d86-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46d86-112">Prompts you for confirmation before running the cmdlet.</span></span>

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
### <span data-ttu-id="46d86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d86-113">-DefaultProfile</span></span>
<span data-ttu-id="46d86-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46d86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46d86-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="46d86-115">-ServerType</span></span>
<span data-ttu-id="46d86-116">列舉描述要連線的伺服器類型的列舉。</span><span class="sxs-lookup"><span data-stu-id="46d86-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="46d86-117">目前支援的值是 sql Server 的 SQL Server 和 SQLDB for SQL Azure 資料庫。</span><span class="sxs-lookup"><span data-stu-id="46d86-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="46d86-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="46d86-118">-AuthType</span></span>
<span data-ttu-id="46d86-119">要用來連線的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="46d86-119">Authentication type to use for connection.</span></span> <span data-ttu-id="46d86-120">可能的值為 SqlAuthentication 和 WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="46d86-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d86-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="46d86-121">-DataSource</span></span>
<span data-ttu-id="46d86-122">要連接的伺服器 address\name。</span><span class="sxs-lookup"><span data-stu-id="46d86-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d86-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="46d86-123">-TrustServerCertificate</span></span>
<span data-ttu-id="46d86-124">布林值，表示保證發生加密。</span><span class="sxs-lookup"><span data-stu-id="46d86-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d86-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d86-125">-WhatIf</span></span>
<span data-ttu-id="46d86-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46d86-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d86-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46d86-127">The cmdlet is not run.</span></span>

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





## <span data-ttu-id="46d86-128">輸入</span><span class="sxs-lookup"><span data-stu-id="46d86-128">INPUTS</span></span>

### <span data-ttu-id="46d86-129">所有</span><span class="sxs-lookup"><span data-stu-id="46d86-129">None</span></span>


## <span data-ttu-id="46d86-130">輸出</span><span class="sxs-lookup"><span data-stu-id="46d86-130">OUTPUTS</span></span>

### <span data-ttu-id="46d86-131">ConnectionInfo 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="46d86-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="46d86-132">筆記</span><span class="sxs-lookup"><span data-stu-id="46d86-132">NOTES</span></span>

## <span data-ttu-id="46d86-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="46d86-133">RELATED LINKS</span></span>

