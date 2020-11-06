---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: 9eb0e0503d1a7a7b71cac8f9f71a7c2f18847bca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447903"
---
# <span data-ttu-id="77972-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="77972-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="77972-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77972-102">SYNOPSIS</span></span>
<span data-ttu-id="77972-103">修改 SQL 資料庫伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="77972-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77972-104">句法</span><span class="sxs-lookup"><span data-stu-id="77972-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77972-105">說明</span><span class="sxs-lookup"><span data-stu-id="77972-105">DESCRIPTION</span></span>
<span data-ttu-id="77972-106">**AzureRmSqlServer** Cmdlet 會修改 Azure SQL 資料庫伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="77972-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="77972-107">示例</span><span class="sxs-lookup"><span data-stu-id="77972-107">EXAMPLES</span></span>

### <span data-ttu-id="77972-108">範例1：重設系統管理員密碼</span><span class="sxs-lookup"><span data-stu-id="77972-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="77972-109">這個命令會在名為 server01 的 AzureSQL 伺服器上重設系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="77972-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="77972-110">參數</span><span class="sxs-lookup"><span data-stu-id="77972-110">PARAMETERS</span></span>

### <span data-ttu-id="77972-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="77972-111">-AssignIdentity</span></span>
<span data-ttu-id="77972-112">針對此伺服器產生並指派 Azure Active Directory 身分識別，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="77972-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77972-113">-Force</span><span class="sxs-lookup"><span data-stu-id="77972-113">-Force</span></span>
<span data-ttu-id="77972-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="77972-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77972-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77972-115">-ResourceGroupName</span></span>
<span data-ttu-id="77972-116">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77972-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="77972-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="77972-117">-ServerName</span></span>
<span data-ttu-id="77972-118">指定此 Cmdlet 修改的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="77972-118">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77972-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="77972-119">-ServerVersion</span></span>
<span data-ttu-id="77972-120">指定此 Cmdlet 變更伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="77972-120">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="77972-121">此參數可接受的值為：2.0 和12.0。</span><span class="sxs-lookup"><span data-stu-id="77972-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77972-122">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="77972-122">-SqlAdministratorPassword</span></span>
<span data-ttu-id="77972-123">針對資料庫伺服器管理員，指定新的密碼（作為 **SecureString** ）。</span><span class="sxs-lookup"><span data-stu-id="77972-123">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="77972-124">若要取得 **SecureString** ，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77972-124">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="77972-125">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="77972-125">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77972-126">-標記</span><span class="sxs-lookup"><span data-stu-id="77972-126">-Tags</span></span>
<span data-ttu-id="77972-127">指定此 Cmdlet 與伺服器關聯的標記字典。</span><span class="sxs-lookup"><span data-stu-id="77972-127">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="77972-128">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="77972-128">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="77972-129">例如：</span><span class="sxs-lookup"><span data-stu-id="77972-129">For example:</span></span>

<span data-ttu-id="77972-130">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="77972-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77972-131">-確認</span><span class="sxs-lookup"><span data-stu-id="77972-131">-Confirm</span></span>
<span data-ttu-id="77972-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77972-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77972-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77972-133">-WhatIf</span></span>
<span data-ttu-id="77972-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77972-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77972-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77972-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77972-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77972-136">-DefaultProfile</span></span>
<span data-ttu-id="77972-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77972-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77972-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77972-138">CommonParameters</span></span>
<span data-ttu-id="77972-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77972-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77972-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77972-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77972-141">輸入</span><span class="sxs-lookup"><span data-stu-id="77972-141">INPUTS</span></span>

## <span data-ttu-id="77972-142">輸出</span><span class="sxs-lookup"><span data-stu-id="77972-142">OUTPUTS</span></span>

### <span data-ttu-id="77972-143">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="77972-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="77972-144">筆記</span><span class="sxs-lookup"><span data-stu-id="77972-144">NOTES</span></span>

## <span data-ttu-id="77972-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="77972-145">RELATED LINKS</span></span>

[<span data-ttu-id="77972-146">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="77972-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
