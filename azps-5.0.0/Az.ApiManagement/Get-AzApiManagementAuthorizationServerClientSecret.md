---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287095"
---
# <span data-ttu-id="16ecb-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="16ecb-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="16ecb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="16ecb-103">取得 API 管理授權伺服器用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="16ecb-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="16ecb-104">句法</span><span class="sxs-lookup"><span data-stu-id="16ecb-104">SYNTAX</span></span>

### <span data-ttu-id="16ecb-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="16ecb-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16ecb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16ecb-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ecb-107">說明</span><span class="sxs-lookup"><span data-stu-id="16ecb-107">DESCRIPTION</span></span>
<span data-ttu-id="16ecb-108">**AzApiManagementAuthorizationServerClientSecret** Cmdlet 會取得 Azure API 管理授權伺服器的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="16ecb-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="16ecb-109">示例</span><span class="sxs-lookup"><span data-stu-id="16ecb-109">EXAMPLES</span></span>

### <span data-ttu-id="16ecb-110">範例1：透過識別碼取得指定的授權伺服器用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="16ecb-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="16ecb-111">這個命令會取得指定的授權伺服器 cient 密碼。</span><span class="sxs-lookup"><span data-stu-id="16ecb-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="16ecb-112">參數</span><span class="sxs-lookup"><span data-stu-id="16ecb-112">PARAMETERS</span></span>

### <span data-ttu-id="16ecb-113">-內容</span><span class="sxs-lookup"><span data-stu-id="16ecb-113">-Context</span></span>
<span data-ttu-id="16ecb-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="16ecb-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="16ecb-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="16ecb-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16ecb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ecb-116">-DefaultProfile</span></span>
<span data-ttu-id="16ecb-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16ecb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ecb-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16ecb-118">-ResourceId</span></span>
<span data-ttu-id="16ecb-119">授權伺服器的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="16ecb-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="16ecb-120">如果已指定，將會嘗試依據識別碼尋找授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="16ecb-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="16ecb-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="16ecb-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ecb-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="16ecb-122">-ServerId</span></span>
<span data-ttu-id="16ecb-123">授權伺服器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="16ecb-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="16ecb-124">如果已指定，則會透過識別碼找到授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="16ecb-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="16ecb-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="16ecb-125">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ecb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ecb-126">CommonParameters</span></span>
<span data-ttu-id="16ecb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16ecb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ecb-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="16ecb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ecb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="16ecb-129">INPUTS</span></span>

### <span data-ttu-id="16ecb-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="16ecb-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="16ecb-131">System.object</span><span class="sxs-lookup"><span data-stu-id="16ecb-131">System.String</span></span>

## <span data-ttu-id="16ecb-132">輸出</span><span class="sxs-lookup"><span data-stu-id="16ecb-132">OUTPUTS</span></span>

### <span data-ttu-id="16ecb-133">ServiceManagement. PsApiManagementClientSecret （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="16ecb-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="16ecb-134">筆記</span><span class="sxs-lookup"><span data-stu-id="16ecb-134">NOTES</span></span>

## <span data-ttu-id="16ecb-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="16ecb-135">RELATED LINKS</span></span>
