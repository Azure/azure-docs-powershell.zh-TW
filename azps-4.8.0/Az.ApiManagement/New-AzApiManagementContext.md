---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969445"
---
# <span data-ttu-id="b185e-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b185e-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="b185e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b185e-102">SYNOPSIS</span></span>
<span data-ttu-id="b185e-103">建立 PsAzureApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b185e-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="b185e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b185e-104">SYNTAX</span></span>

### <span data-ttu-id="b185e-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b185e-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b185e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b185e-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b185e-107">說明</span><span class="sxs-lookup"><span data-stu-id="b185e-107">DESCRIPTION</span></span>
<span data-ttu-id="b185e-108">**新的-AzApiManagementCoNtext** Cmdlet 會建立 **PsAzureApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="b185e-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="b185e-109">此內容用於所有 API 管理服務 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b185e-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="b185e-110">示例</span><span class="sxs-lookup"><span data-stu-id="b185e-110">EXAMPLES</span></span>

### <span data-ttu-id="b185e-111">範例1：建立 PsApiManagementCoNtext 實例</span><span class="sxs-lookup"><span data-stu-id="b185e-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="b185e-112">這個命令會建立 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="b185e-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="b185e-113">參數</span><span class="sxs-lookup"><span data-stu-id="b185e-113">PARAMETERS</span></span>

### <span data-ttu-id="b185e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b185e-114">-DefaultProfile</span></span>
<span data-ttu-id="b185e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b185e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b185e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b185e-116">-ResourceGroupName</span></span>
<span data-ttu-id="b185e-117">指定部署 API 管理服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b185e-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="b185e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b185e-118">-ResourceId</span></span>
<span data-ttu-id="b185e-119">ApiManagement 服務的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b185e-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="b185e-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="b185e-120">This parameter is required.</span></span>

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

### <span data-ttu-id="b185e-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b185e-121">-ServiceName</span></span>
<span data-ttu-id="b185e-122">指定已部署 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="b185e-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="b185e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b185e-123">CommonParameters</span></span>
<span data-ttu-id="b185e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b185e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b185e-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b185e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b185e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b185e-126">INPUTS</span></span>

### <span data-ttu-id="b185e-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b185e-127">System.String</span></span>

## <span data-ttu-id="b185e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b185e-128">OUTPUTS</span></span>

### <span data-ttu-id="b185e-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b185e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b185e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b185e-130">NOTES</span></span>

## <span data-ttu-id="b185e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b185e-131">RELATED LINKS</span></span>
