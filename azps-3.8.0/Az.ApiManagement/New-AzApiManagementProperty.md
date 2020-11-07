---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: bed6126dbd1ea57a29d041daf10a3deb05f2dc92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958163"
---
# <span data-ttu-id="45fbc-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="45fbc-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="45fbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="45fbc-103">建立新的屬性。</span><span class="sxs-lookup"><span data-stu-id="45fbc-103">Creates a new Property.</span></span>

## <span data-ttu-id="45fbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="45fbc-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45fbc-105">說明</span><span class="sxs-lookup"><span data-stu-id="45fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="45fbc-106">**新的-AzApiManagementProperty** Cmdlet 會建立 Azure API 管理 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="45fbc-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="45fbc-107">示例</span><span class="sxs-lookup"><span data-stu-id="45fbc-107">EXAMPLES</span></span>

### <span data-ttu-id="45fbc-108">範例1：建立包含標記的屬性</span><span class="sxs-lookup"><span data-stu-id="45fbc-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="45fbc-109">第一個命令會將兩個值指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="45fbc-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="45fbc-110">第二個命令會建立屬性，並將 $Tags 中的字串指定為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="45fbc-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="45fbc-111">範例2：建立具有機密值的屬性</span><span class="sxs-lookup"><span data-stu-id="45fbc-111">Example 2: Create a property that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="45fbc-112">這個命令會建立具有已加密之值的 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="45fbc-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="45fbc-113">參數</span><span class="sxs-lookup"><span data-stu-id="45fbc-113">PARAMETERS</span></span>

### <span data-ttu-id="45fbc-114">-內容</span><span class="sxs-lookup"><span data-stu-id="45fbc-114">-Context</span></span>
<span data-ttu-id="45fbc-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="45fbc-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="45fbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fbc-116">-DefaultProfile</span></span>
<span data-ttu-id="45fbc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45fbc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45fbc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="45fbc-118">-Name</span></span>
<span data-ttu-id="45fbc-119">指定此 Cmdlet 所建立之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="45fbc-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="45fbc-120">最大長度為100個字元。</span><span class="sxs-lookup"><span data-stu-id="45fbc-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="45fbc-121">名稱只包含字母、數位、句點、破折號及底線字元。</span><span class="sxs-lookup"><span data-stu-id="45fbc-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="45fbc-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="45fbc-122">-PropertyId</span></span>
<span data-ttu-id="45fbc-123">指定屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="45fbc-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="45fbc-124">最大長度為256個字元。</span><span class="sxs-lookup"><span data-stu-id="45fbc-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="45fbc-125">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="45fbc-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="45fbc-126">密碼</span><span class="sxs-lookup"><span data-stu-id="45fbc-126">-Secret</span></span>
<span data-ttu-id="45fbc-127">表示屬性值是一個機密，應該經過加密。</span><span class="sxs-lookup"><span data-stu-id="45fbc-127">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fbc-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="45fbc-128">-Tag</span></span>
<span data-ttu-id="45fbc-129">要與屬性相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="45fbc-129">Tags to be associated with Property.</span></span> <span data-ttu-id="45fbc-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="45fbc-130">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fbc-131">-值</span><span class="sxs-lookup"><span data-stu-id="45fbc-131">-Value</span></span>
<span data-ttu-id="45fbc-132">指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="45fbc-132">Specifies a value for the property.</span></span>
<span data-ttu-id="45fbc-133">這個值可以包含原則運算式。</span><span class="sxs-lookup"><span data-stu-id="45fbc-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="45fbc-134">最大長度為1000個字元。</span><span class="sxs-lookup"><span data-stu-id="45fbc-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="45fbc-135">此值可能不是空白，或是只由空格所組成。</span><span class="sxs-lookup"><span data-stu-id="45fbc-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="45fbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fbc-136">CommonParameters</span></span>
<span data-ttu-id="45fbc-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45fbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fbc-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="45fbc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fbc-139">輸入</span><span class="sxs-lookup"><span data-stu-id="45fbc-139">INPUTS</span></span>

### <span data-ttu-id="45fbc-140">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="45fbc-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45fbc-141">System.object</span><span class="sxs-lookup"><span data-stu-id="45fbc-141">System.String</span></span>

### <span data-ttu-id="45fbc-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="45fbc-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="45fbc-143">System.object []</span><span class="sxs-lookup"><span data-stu-id="45fbc-143">System.String[]</span></span>

## <span data-ttu-id="45fbc-144">輸出</span><span class="sxs-lookup"><span data-stu-id="45fbc-144">OUTPUTS</span></span>

### <span data-ttu-id="45fbc-145">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="45fbc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="45fbc-146">筆記</span><span class="sxs-lookup"><span data-stu-id="45fbc-146">NOTES</span></span>

## <span data-ttu-id="45fbc-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="45fbc-147">RELATED LINKS</span></span>

[<span data-ttu-id="45fbc-148">移除-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="45fbc-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="45fbc-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="45fbc-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


