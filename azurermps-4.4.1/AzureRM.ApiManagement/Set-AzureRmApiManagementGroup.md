---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454943"
---
# <span data-ttu-id="08a05-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="08a05-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="08a05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08a05-102">SYNOPSIS</span></span>
<span data-ttu-id="08a05-103">配置 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="08a05-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08a05-104">句法</span><span class="sxs-lookup"><span data-stu-id="08a05-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08a05-105">說明</span><span class="sxs-lookup"><span data-stu-id="08a05-105">DESCRIPTION</span></span>
<span data-ttu-id="08a05-106">AzureRmApiManagementGroup Cmdlet 會 **設定** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="08a05-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="08a05-107">示例</span><span class="sxs-lookup"><span data-stu-id="08a05-107">EXAMPLES</span></span>

### <span data-ttu-id="08a05-108">範例1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="08a05-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="08a05-109">這個命令會設定一個名為 Group0001 的管理群組。</span><span class="sxs-lookup"><span data-stu-id="08a05-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="08a05-110">參數</span><span class="sxs-lookup"><span data-stu-id="08a05-110">PARAMETERS</span></span>

### <span data-ttu-id="08a05-111">-內容</span><span class="sxs-lookup"><span data-stu-id="08a05-111">-Context</span></span>
<span data-ttu-id="08a05-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="08a05-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="08a05-113">-描述</span><span class="sxs-lookup"><span data-stu-id="08a05-113">-Description</span></span>
<span data-ttu-id="08a05-114">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="08a05-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="08a05-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="08a05-115">-GroupId</span></span>
<span data-ttu-id="08a05-116">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="08a05-116">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="08a05-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="08a05-117">-Name</span></span>
<span data-ttu-id="08a05-118">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08a05-118">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="08a05-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08a05-119">-PassThru</span></span>
<span data-ttu-id="08a05-120">passthru</span><span class="sxs-lookup"><span data-stu-id="08a05-120">passthru</span></span>

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

### <span data-ttu-id="08a05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a05-121">-DefaultProfile</span></span>
<span data-ttu-id="08a05-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08a05-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08a05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a05-123">CommonParameters</span></span>
<span data-ttu-id="08a05-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08a05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a05-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08a05-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a05-126">輸入</span><span class="sxs-lookup"><span data-stu-id="08a05-126">INPUTS</span></span>

## <span data-ttu-id="08a05-127">輸出</span><span class="sxs-lookup"><span data-stu-id="08a05-127">OUTPUTS</span></span>

### <span data-ttu-id="08a05-128">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="08a05-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="08a05-129">筆記</span><span class="sxs-lookup"><span data-stu-id="08a05-129">NOTES</span></span>

## <span data-ttu-id="08a05-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="08a05-130">RELATED LINKS</span></span>

[<span data-ttu-id="08a05-131">AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="08a05-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="08a05-132">新-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="08a05-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="08a05-133">移除-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="08a05-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


