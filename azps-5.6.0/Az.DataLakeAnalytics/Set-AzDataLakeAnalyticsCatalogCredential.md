---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 51af3aeffe5cf75835507e78b4638270b255fb29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911122"
---
# <span data-ttu-id="ddc87-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="ddc87-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="ddc87-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddc87-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc87-103">修改 Azure Data Lake Analytics 目錄認證密碼。</span><span class="sxs-lookup"><span data-stu-id="ddc87-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="ddc87-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddc87-104">SYNTAX</span></span>

### <span data-ttu-id="ddc87-105">SetByHostNameAndPort (預設) </span><span class="sxs-lookup"><span data-stu-id="ddc87-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc87-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="ddc87-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc87-107">描述</span><span class="sxs-lookup"><span data-stu-id="ddc87-107">DESCRIPTION</span></span>
<span data-ttu-id="ddc87-108">此Set-AzDataLakeAnalyticsCatalogCredential Cmdlet 會修改與 Azure Data Lake Analytics 目錄相關聯的認證密碼。</span><span class="sxs-lookup"><span data-stu-id="ddc87-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="ddc87-109">例子</span><span class="sxs-lookup"><span data-stu-id="ddc87-109">EXAMPLES</span></span>

### <span data-ttu-id="ddc87-110">範例 1：修改與帳戶相關聯的認證密碼</span><span class="sxs-lookup"><span data-stu-id="ddc87-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="ddc87-111">此命令將認證密碼設定為 NewPassword 中指定的密碼。</span><span class="sxs-lookup"><span data-stu-id="ddc87-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="ddc87-112">參數</span><span class="sxs-lookup"><span data-stu-id="ddc87-112">PARAMETERS</span></span>

### <span data-ttu-id="ddc87-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="ddc87-113">-Account</span></span>
<span data-ttu-id="ddc87-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc87-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-115">-認證</span><span class="sxs-lookup"><span data-stu-id="ddc87-115">-Credential</span></span>
<span data-ttu-id="ddc87-116">指定要修改之認證的名稱和目前密碼。</span><span class="sxs-lookup"><span data-stu-id="ddc87-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ddc87-117">-CredentialName</span></span>
<span data-ttu-id="ddc87-118">指定要修改的認證名稱</span><span class="sxs-lookup"><span data-stu-id="ddc87-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="ddc87-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="ddc87-119">-DatabaseHost</span></span>
<span data-ttu-id="ddc87-120">指定認證可以連結之外部資料源的主機名稱，其格式mydatabase.contoso.com。</span><span class="sxs-lookup"><span data-stu-id="ddc87-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddc87-121">-DatabaseName</span></span>
<span data-ttu-id="ddc87-122">指定資料湖分析帳戶中持有認證的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc87-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="ddc87-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc87-123">-DefaultProfile</span></span>
<span data-ttu-id="ddc87-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ddc87-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddc87-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="ddc87-125">-NewPassword</span></span>
<span data-ttu-id="ddc87-126">指定認證的新密碼</span><span class="sxs-lookup"><span data-stu-id="ddc87-126">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-127">-埠</span><span class="sxs-lookup"><span data-stu-id="ddc87-127">-Port</span></span>
<span data-ttu-id="ddc87-128">指定使用此認證連接至指定 DatabaseHost 的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="ddc87-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="ddc87-129">-Uri</span></span>
<span data-ttu-id="ddc87-130">指定此認證可 (外部) URI 識別碼的完整統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="ddc87-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ddc87-131">-Confirm</span></span>
<span data-ttu-id="ddc87-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ddc87-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc87-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc87-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc87-134">CommonParameters</span></span>
<span data-ttu-id="ddc87-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddc87-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc87-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ddc87-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc87-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ddc87-137">INPUTS</span></span>

### <span data-ttu-id="ddc87-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ddc87-138">System.String</span></span>

### <span data-ttu-id="ddc87-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="ddc87-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ddc87-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="ddc87-140">System.Uri</span></span>

### <span data-ttu-id="ddc87-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ddc87-141">System.Int32</span></span>

## <span data-ttu-id="ddc87-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ddc87-142">OUTPUTS</span></span>

### <span data-ttu-id="ddc87-143">Microsoft.Azure.management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="ddc87-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="ddc87-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ddc87-144">NOTES</span></span>

## <span data-ttu-id="ddc87-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddc87-145">RELATED LINKS</span></span>
