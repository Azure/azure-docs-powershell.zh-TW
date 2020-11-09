---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287091"
---
# <span data-ttu-id="15d28-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="15d28-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="15d28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15d28-102">SYNOPSIS</span></span>
<span data-ttu-id="15d28-103">取得特定命名值的機密值。</span><span class="sxs-lookup"><span data-stu-id="15d28-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="15d28-104">句法</span><span class="sxs-lookup"><span data-stu-id="15d28-104">SYNTAX</span></span>

### <span data-ttu-id="15d28-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="15d28-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d28-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="15d28-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d28-107">說明</span><span class="sxs-lookup"><span data-stu-id="15d28-107">DESCRIPTION</span></span>
<span data-ttu-id="15d28-108">取得特定命名值的機密值。</span><span class="sxs-lookup"><span data-stu-id="15d28-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="15d28-109">示例</span><span class="sxs-lookup"><span data-stu-id="15d28-109">EXAMPLES</span></span>

### <span data-ttu-id="15d28-110">範例1：透過名稱取得命名值</span><span class="sxs-lookup"><span data-stu-id="15d28-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="15d28-111">這個命令會在指定的值名稱中取得已命名的值詳細資料。</span><span class="sxs-lookup"><span data-stu-id="15d28-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="15d28-112">參數</span><span class="sxs-lookup"><span data-stu-id="15d28-112">PARAMETERS</span></span>

### <span data-ttu-id="15d28-113">-內容</span><span class="sxs-lookup"><span data-stu-id="15d28-113">-Context</span></span>
<span data-ttu-id="15d28-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="15d28-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="15d28-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="15d28-115">This parameter is required.</span></span>

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

### <span data-ttu-id="15d28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d28-116">-DefaultProfile</span></span>
<span data-ttu-id="15d28-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15d28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d28-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="15d28-118">-NamedValueId</span></span>
<span data-ttu-id="15d28-119">命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="15d28-119">Identifier of a the named value.</span></span>
<span data-ttu-id="15d28-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="15d28-120">This parameter is required.</span></span>

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

### <span data-ttu-id="15d28-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d28-121">CommonParameters</span></span>
<span data-ttu-id="15d28-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15d28-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d28-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="15d28-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d28-124">輸入</span><span class="sxs-lookup"><span data-stu-id="15d28-124">INPUTS</span></span>

### <span data-ttu-id="15d28-125">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="15d28-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15d28-126">System.object</span><span class="sxs-lookup"><span data-stu-id="15d28-126">System.String</span></span>

## <span data-ttu-id="15d28-127">輸出</span><span class="sxs-lookup"><span data-stu-id="15d28-127">OUTPUTS</span></span>

### <span data-ttu-id="15d28-128">ServiceManagement. PsApiManagementNamedValueSecretValue （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="15d28-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="15d28-129">筆記</span><span class="sxs-lookup"><span data-stu-id="15d28-129">NOTES</span></span>

## <span data-ttu-id="15d28-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="15d28-130">RELATED LINKS</span></span>
