---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: ad6e2aebcc5a4edcf5acd3255385b0e78f317627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611612"
---
# <span data-ttu-id="b4e14-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b4e14-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="b4e14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4e14-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e14-103"> (命名值) 取得清單或特定屬性。</span><span class="sxs-lookup"><span data-stu-id="b4e14-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="b4e14-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4e14-104">SYNTAX</span></span>

### <span data-ttu-id="b4e14-105">GetAllProperties (預設) </span><span class="sxs-lookup"><span data-stu-id="b4e14-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e14-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="b4e14-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4e14-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="b4e14-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4e14-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="b4e14-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e14-109">說明</span><span class="sxs-lookup"><span data-stu-id="b4e14-109">DESCRIPTION</span></span>
<span data-ttu-id="b4e14-110">**AzApiManagementProperty** Cmdlet 會取得清單或特定屬性。</span><span class="sxs-lookup"><span data-stu-id="b4e14-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="b4e14-111">示例</span><span class="sxs-lookup"><span data-stu-id="b4e14-111">EXAMPLES</span></span>

### <span data-ttu-id="b4e14-112">範例1：透過名稱取得屬性</span><span class="sxs-lookup"><span data-stu-id="b4e14-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="b4e14-113">參數</span><span class="sxs-lookup"><span data-stu-id="b4e14-113">PARAMETERS</span></span>

### <span data-ttu-id="b4e14-114">-內容</span><span class="sxs-lookup"><span data-stu-id="b4e14-114">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e14-115">-DefaultProfile</span></span>
<span data-ttu-id="b4e14-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4e14-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4e14-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4e14-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e14-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="b4e14-118">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e14-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4e14-119">-Tag</span></span>
<span data-ttu-id="b4e14-120">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="b4e14-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4e14-121">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b4e14-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e14-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e14-122">CommonParameters</span></span>
<span data-ttu-id="b4e14-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4e14-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e14-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4e14-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e14-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b4e14-125">INPUTS</span></span>

### <span data-ttu-id="b4e14-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b4e14-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4e14-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b4e14-127">System.String</span></span>

## <span data-ttu-id="b4e14-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b4e14-128">OUTPUTS</span></span>

### <span data-ttu-id="b4e14-129">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b4e14-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="b4e14-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b4e14-130">NOTES</span></span>

## <span data-ttu-id="b4e14-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4e14-131">RELATED LINKS</span></span>
