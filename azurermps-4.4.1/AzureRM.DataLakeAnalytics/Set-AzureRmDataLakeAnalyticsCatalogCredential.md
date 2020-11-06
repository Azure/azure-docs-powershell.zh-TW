---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: e82559ec366809613ba66af4c27a3b944869f074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453563"
---
# <span data-ttu-id="e957c-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="e957c-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="e957c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e957c-102">SYNOPSIS</span></span>
<span data-ttu-id="e957c-103">修改 Azure Data Lake Analytics 目錄認證密碼。</span><span class="sxs-lookup"><span data-stu-id="e957c-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e957c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e957c-104">SYNTAX</span></span>

### <span data-ttu-id="e957c-105">指定 [主機名稱] 和 [埠] (預設) </span><span class="sxs-lookup"><span data-stu-id="e957c-105">Specify host name and port (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e957c-106">指定完整 URI</span><span class="sxs-lookup"><span data-stu-id="e957c-106">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e957c-107">說明</span><span class="sxs-lookup"><span data-stu-id="e957c-107">DESCRIPTION</span></span>
<span data-ttu-id="e957c-108">Set-AzureRmDataLakeAnalyticsCatalogCredential Cmdlet 會修改與 Azure Data Lake Analytics 目錄相關聯的認證密碼。</span><span class="sxs-lookup"><span data-stu-id="e957c-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="e957c-109">示例</span><span class="sxs-lookup"><span data-stu-id="e957c-109">EXAMPLES</span></span>

### <span data-ttu-id="e957c-110">範例1：修改與帳戶相關聯的認證密碼</span><span class="sxs-lookup"><span data-stu-id="e957c-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="e957c-111">這個命令會將認證密碼設定為 NewPassword 中指定的密碼。</span><span class="sxs-lookup"><span data-stu-id="e957c-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="e957c-112">參數</span><span class="sxs-lookup"><span data-stu-id="e957c-112">PARAMETERS</span></span>

### <span data-ttu-id="e957c-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e957c-113">-Account</span></span>
<span data-ttu-id="e957c-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e957c-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e957c-115">-認證</span><span class="sxs-lookup"><span data-stu-id="e957c-115">-Credential</span></span>
<span data-ttu-id="e957c-116">指定要修改之認證的名稱和目前密碼。</span><span class="sxs-lookup"><span data-stu-id="e957c-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="e957c-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e957c-117">-CredentialName</span></span>
<span data-ttu-id="e957c-118">指定要修改的認證名稱</span><span class="sxs-lookup"><span data-stu-id="e957c-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="e957c-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="e957c-119">-DatabaseHost</span></span>
<span data-ttu-id="e957c-120">指定認證可以連線至 mydatabase.contoso.com [格式] 的外部資料源的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="e957c-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e957c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e957c-121">-DatabaseName</span></span>
<span data-ttu-id="e957c-122">在包含認證的 Data Lake Analytics 帳戶中指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e957c-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="e957c-123">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="e957c-123">-NewPassword</span></span>
<span data-ttu-id="e957c-124">指定認證的新密碼</span><span class="sxs-lookup"><span data-stu-id="e957c-124">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="e957c-125">-埠</span><span class="sxs-lookup"><span data-stu-id="e957c-125">-Port</span></span>
<span data-ttu-id="e957c-126">指定使用此認證連接至指定 DatabaseHost 的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="e957c-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e957c-127">-Uri</span><span class="sxs-lookup"><span data-stu-id="e957c-127">-Uri</span></span>
<span data-ttu-id="e957c-128">指定此認證可連線的外部資料源 (URI) 的完整統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="e957c-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e957c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e957c-129">-Confirm</span></span>
<span data-ttu-id="e957c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e957c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e957c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e957c-131">-WhatIf</span></span>
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

### <span data-ttu-id="e957c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e957c-132">-DefaultProfile</span></span>
<span data-ttu-id="e957c-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e957c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e957c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e957c-134">CommonParameters</span></span>
<span data-ttu-id="e957c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e957c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e957c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e957c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e957c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e957c-137">INPUTS</span></span>

## <span data-ttu-id="e957c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e957c-138">OUTPUTS</span></span>

### <span data-ttu-id="e957c-139">所有</span><span class="sxs-lookup"><span data-stu-id="e957c-139">None</span></span>

## <span data-ttu-id="e957c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e957c-140">NOTES</span></span>

## <span data-ttu-id="e957c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e957c-141">RELATED LINKS</span></span>

