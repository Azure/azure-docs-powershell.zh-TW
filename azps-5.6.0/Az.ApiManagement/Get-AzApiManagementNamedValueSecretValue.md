---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 1ef17239338319696d08a316648a158039fa63f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907825"
---
# <span data-ttu-id="aef30-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="aef30-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="aef30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aef30-102">SYNOPSIS</span></span>
<span data-ttu-id="aef30-103">獲得特定已命名值的機密值。</span><span class="sxs-lookup"><span data-stu-id="aef30-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="aef30-104">語法</span><span class="sxs-lookup"><span data-stu-id="aef30-104">SYNTAX</span></span>

### <span data-ttu-id="aef30-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="aef30-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aef30-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="aef30-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aef30-107">描述</span><span class="sxs-lookup"><span data-stu-id="aef30-107">DESCRIPTION</span></span>
<span data-ttu-id="aef30-108">獲得特定已命名值的機密值。</span><span class="sxs-lookup"><span data-stu-id="aef30-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="aef30-109">例子</span><span class="sxs-lookup"><span data-stu-id="aef30-109">EXAMPLES</span></span>

### <span data-ttu-id="aef30-110">範例 1：根據名稱取得命名值</span><span class="sxs-lookup"><span data-stu-id="aef30-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="aef30-111">此命令會獲得指定值名稱的命名值詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aef30-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="aef30-112">參數</span><span class="sxs-lookup"><span data-stu-id="aef30-112">PARAMETERS</span></span>

### <span data-ttu-id="aef30-113">-內容</span><span class="sxs-lookup"><span data-stu-id="aef30-113">-Context</span></span>
<span data-ttu-id="aef30-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="aef30-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aef30-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="aef30-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aef30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef30-116">-DefaultProfile</span></span>
<span data-ttu-id="aef30-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aef30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aef30-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="aef30-118">-NamedValueId</span></span>
<span data-ttu-id="aef30-119">已命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aef30-119">Identifier of a the named value.</span></span>
<span data-ttu-id="aef30-120">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="aef30-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef30-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef30-121">CommonParameters</span></span>
<span data-ttu-id="aef30-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aef30-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef30-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aef30-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef30-124">輸入</span><span class="sxs-lookup"><span data-stu-id="aef30-124">INPUTS</span></span>

### <span data-ttu-id="aef30-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="aef30-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aef30-126">System.String</span><span class="sxs-lookup"><span data-stu-id="aef30-126">System.String</span></span>

## <span data-ttu-id="aef30-127">輸出</span><span class="sxs-lookup"><span data-stu-id="aef30-127">OUTPUTS</span></span>

### <span data-ttu-id="aef30-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="aef30-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="aef30-129">筆記</span><span class="sxs-lookup"><span data-stu-id="aef30-129">NOTES</span></span>

## <span data-ttu-id="aef30-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="aef30-130">RELATED LINKS</span></span>
