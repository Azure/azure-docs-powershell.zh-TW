---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 058a82398be387913a0dd3eaf58c80ac12b692dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445823"
---
# <span data-ttu-id="70c67-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70c67-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="70c67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70c67-102">SYNOPSIS</span></span>
<span data-ttu-id="70c67-103">配置 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="70c67-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70c67-104">句法</span><span class="sxs-lookup"><span data-stu-id="70c67-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70c67-105">說明</span><span class="sxs-lookup"><span data-stu-id="70c67-105">DESCRIPTION</span></span>
<span data-ttu-id="70c67-106">AzureRmApiManagementGroup Cmdlet 會 **設定** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="70c67-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="70c67-107">示例</span><span class="sxs-lookup"><span data-stu-id="70c67-107">EXAMPLES</span></span>

### <span data-ttu-id="70c67-108">範例1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="70c67-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="70c67-109">這個命令會設定一個名為 Group0001 的管理群組。</span><span class="sxs-lookup"><span data-stu-id="70c67-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="70c67-110">參數</span><span class="sxs-lookup"><span data-stu-id="70c67-110">PARAMETERS</span></span>

### <span data-ttu-id="70c67-111">-內容</span><span class="sxs-lookup"><span data-stu-id="70c67-111">-Context</span></span>
<span data-ttu-id="70c67-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="70c67-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="70c67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c67-113">-DefaultProfile</span></span>
<span data-ttu-id="70c67-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70c67-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70c67-115">-描述</span><span class="sxs-lookup"><span data-stu-id="70c67-115">-Description</span></span>
<span data-ttu-id="70c67-116">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="70c67-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="70c67-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="70c67-117">-GroupId</span></span>
<span data-ttu-id="70c67-118">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="70c67-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="70c67-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="70c67-119">-Name</span></span>
<span data-ttu-id="70c67-120">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c67-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="70c67-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70c67-121">-PassThru</span></span>
<span data-ttu-id="70c67-122">passthru</span><span class="sxs-lookup"><span data-stu-id="70c67-122">passthru</span></span>

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

### <span data-ttu-id="70c67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c67-123">CommonParameters</span></span>
<span data-ttu-id="70c67-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70c67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c67-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70c67-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c67-126">輸入</span><span class="sxs-lookup"><span data-stu-id="70c67-126">INPUTS</span></span>

### <span data-ttu-id="70c67-127">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="70c67-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="70c67-128">System.object</span><span class="sxs-lookup"><span data-stu-id="70c67-128">System.String</span></span>

### <span data-ttu-id="70c67-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="70c67-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="70c67-130">輸出</span><span class="sxs-lookup"><span data-stu-id="70c67-130">OUTPUTS</span></span>

### <span data-ttu-id="70c67-131">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="70c67-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="70c67-132">筆記</span><span class="sxs-lookup"><span data-stu-id="70c67-132">NOTES</span></span>

## <span data-ttu-id="70c67-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="70c67-133">RELATED LINKS</span></span>

[<span data-ttu-id="70c67-134">AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70c67-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="70c67-135">新-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70c67-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="70c67-136">移除-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70c67-136">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


