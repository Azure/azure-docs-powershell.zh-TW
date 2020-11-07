---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958185"
---
# <span data-ttu-id="f4505-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f4505-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="f4505-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4505-102">SYNOPSIS</span></span>
<span data-ttu-id="f4505-103">建立 PsAzureApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f4505-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="f4505-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4505-104">SYNTAX</span></span>

### <span data-ttu-id="f4505-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f4505-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4505-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4505-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4505-107">說明</span><span class="sxs-lookup"><span data-stu-id="f4505-107">DESCRIPTION</span></span>
<span data-ttu-id="f4505-108">**新的-AzApiManagementCoNtext** Cmdlet 會建立 **PsAzureApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="f4505-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="f4505-109">此內容用於所有 API 管理服務 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4505-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="f4505-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4505-110">EXAMPLES</span></span>

### <span data-ttu-id="f4505-111">範例1：建立 PsApiManagementCoNtext 實例</span><span class="sxs-lookup"><span data-stu-id="f4505-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="f4505-112">這個命令會建立 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="f4505-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="f4505-113">參數</span><span class="sxs-lookup"><span data-stu-id="f4505-113">PARAMETERS</span></span>

### <span data-ttu-id="f4505-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4505-114">-DefaultProfile</span></span>
<span data-ttu-id="f4505-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4505-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4505-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4505-116">-ResourceGroupName</span></span>
<span data-ttu-id="f4505-117">指定部署 API 管理服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4505-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4505-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4505-118">-ResourceId</span></span>
<span data-ttu-id="f4505-119">ApiManagement 服務的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4505-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="f4505-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f4505-120">This parameter is required.</span></span>

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

### <span data-ttu-id="f4505-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f4505-121">-ServiceName</span></span>
<span data-ttu-id="f4505-122">指定已部署 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4505-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4505-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4505-123">CommonParameters</span></span>
<span data-ttu-id="f4505-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4505-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4505-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4505-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4505-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f4505-126">INPUTS</span></span>

### <span data-ttu-id="f4505-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f4505-127">System.String</span></span>

## <span data-ttu-id="f4505-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f4505-128">OUTPUTS</span></span>

### <span data-ttu-id="f4505-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f4505-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="f4505-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f4505-130">NOTES</span></span>

## <span data-ttu-id="f4505-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4505-131">RELATED LINKS</span></span>
