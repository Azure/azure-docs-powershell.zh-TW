---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449421"
---
# <span data-ttu-id="27be6-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27be6-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="27be6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27be6-102">SYNOPSIS</span></span>
<span data-ttu-id="27be6-103">配置 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="27be6-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27be6-104">句法</span><span class="sxs-lookup"><span data-stu-id="27be6-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27be6-105">說明</span><span class="sxs-lookup"><span data-stu-id="27be6-105">DESCRIPTION</span></span>
<span data-ttu-id="27be6-106">AzureRmApiManagementGroup Cmdlet 會 **設定** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="27be6-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="27be6-107">示例</span><span class="sxs-lookup"><span data-stu-id="27be6-107">EXAMPLES</span></span>

### <span data-ttu-id="27be6-108">範例1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="27be6-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="27be6-109">這個命令會設定一個名為 Group0001 的管理群組。</span><span class="sxs-lookup"><span data-stu-id="27be6-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="27be6-110">參數</span><span class="sxs-lookup"><span data-stu-id="27be6-110">PARAMETERS</span></span>

### <span data-ttu-id="27be6-111">-內容</span><span class="sxs-lookup"><span data-stu-id="27be6-111">-Context</span></span>
<span data-ttu-id="27be6-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="27be6-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27be6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27be6-113">-DefaultProfile</span></span>
<span data-ttu-id="27be6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27be6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27be6-115">-描述</span><span class="sxs-lookup"><span data-stu-id="27be6-115">-Description</span></span>
<span data-ttu-id="27be6-116">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="27be6-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27be6-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="27be6-117">-GroupId</span></span>
<span data-ttu-id="27be6-118">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27be6-118">Specifies the identifier of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27be6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="27be6-119">-Name</span></span>
<span data-ttu-id="27be6-120">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27be6-120">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27be6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27be6-121">-PassThru</span></span>
<span data-ttu-id="27be6-122">passthru</span><span class="sxs-lookup"><span data-stu-id="27be6-122">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27be6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27be6-123">CommonParameters</span></span>
<span data-ttu-id="27be6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27be6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27be6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27be6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27be6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="27be6-126">INPUTS</span></span>

### <span data-ttu-id="27be6-127">所有</span><span class="sxs-lookup"><span data-stu-id="27be6-127">None</span></span>
<span data-ttu-id="27be6-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="27be6-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27be6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="27be6-129">OUTPUTS</span></span>

### <span data-ttu-id="27be6-130">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="27be6-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="27be6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="27be6-131">NOTES</span></span>

## <span data-ttu-id="27be6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="27be6-132">RELATED LINKS</span></span>

[<span data-ttu-id="27be6-133">AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27be6-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="27be6-134">新-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27be6-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="27be6-135">移除-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27be6-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


