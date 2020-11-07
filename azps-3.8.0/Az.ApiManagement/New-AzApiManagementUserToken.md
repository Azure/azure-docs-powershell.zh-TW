---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 5b8c781380ced5ed174c094cf1ff66a8eb820309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957863"
---
# <span data-ttu-id="551be-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="551be-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="551be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="551be-102">SYNOPSIS</span></span>
<span data-ttu-id="551be-103">產生使用者的共用存取權杖。</span><span class="sxs-lookup"><span data-stu-id="551be-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="551be-104">句法</span><span class="sxs-lookup"><span data-stu-id="551be-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="551be-105">說明</span><span class="sxs-lookup"><span data-stu-id="551be-105">DESCRIPTION</span></span>
<span data-ttu-id="551be-106">Cmdlet **AzApiManagementUserToken** 會產生指定使用者的共用存取權杖</span><span class="sxs-lookup"><span data-stu-id="551be-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="551be-107">示例</span><span class="sxs-lookup"><span data-stu-id="551be-107">EXAMPLES</span></span>

### <span data-ttu-id="551be-108">範例1：針對 Git 使用者產生共用存取權杖</span><span class="sxs-lookup"><span data-stu-id="551be-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="551be-109">此腳本會取得在 ApiManagement service 中設定的 Git 使用者，並使用有效期為8小時的主鍵來產生共用存取權杖。</span><span class="sxs-lookup"><span data-stu-id="551be-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="551be-110">參數</span><span class="sxs-lookup"><span data-stu-id="551be-110">PARAMETERS</span></span>

### <span data-ttu-id="551be-111">-內容</span><span class="sxs-lookup"><span data-stu-id="551be-111">-Context</span></span>
<span data-ttu-id="551be-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="551be-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="551be-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="551be-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="551be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551be-114">-DefaultProfile</span></span>
<span data-ttu-id="551be-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="551be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="551be-116">-到期日</span><span class="sxs-lookup"><span data-stu-id="551be-116">-Expiry</span></span>
<span data-ttu-id="551be-117">權杖到期。</span><span class="sxs-lookup"><span data-stu-id="551be-117">Expiry of the Token.</span></span>
<span data-ttu-id="551be-118">如果未指定，權杖會建立為在8小時後到期。</span><span class="sxs-lookup"><span data-stu-id="551be-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="551be-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="551be-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551be-120">-KeyType</span><span class="sxs-lookup"><span data-stu-id="551be-120">-KeyType</span></span>
<span data-ttu-id="551be-121">產生權杖時要使用的使用者金鑰。</span><span class="sxs-lookup"><span data-stu-id="551be-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="551be-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="551be-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551be-123">-UserId</span><span class="sxs-lookup"><span data-stu-id="551be-123">-UserId</span></span>
<span data-ttu-id="551be-124">現有使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="551be-124">Identifier of existing user.</span></span>
<span data-ttu-id="551be-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="551be-125">This parameter is required.</span></span>

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

### <span data-ttu-id="551be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551be-126">CommonParameters</span></span>
<span data-ttu-id="551be-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="551be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551be-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="551be-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551be-129">輸入</span><span class="sxs-lookup"><span data-stu-id="551be-129">INPUTS</span></span>

### <span data-ttu-id="551be-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="551be-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="551be-131">System.object</span><span class="sxs-lookup"><span data-stu-id="551be-131">System.String</span></span>

### <span data-ttu-id="551be-132">ServiceManagement. PsApiManagementUserKeyType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="551be-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="551be-133">系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="551be-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="551be-134">輸出</span><span class="sxs-lookup"><span data-stu-id="551be-134">OUTPUTS</span></span>

### <span data-ttu-id="551be-135">ServiceManagement. PsApiManagementUserToken （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="551be-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="551be-136">筆記</span><span class="sxs-lookup"><span data-stu-id="551be-136">NOTES</span></span>

## <span data-ttu-id="551be-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="551be-137">RELATED LINKS</span></span>
