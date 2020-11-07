---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788765"
---
# <span data-ttu-id="fc5e0-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fc5e0-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="fc5e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5e0-103">配置 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-103">Configures an API management group.</span></span>

## <span data-ttu-id="fc5e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc5e0-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc5e0-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc5e0-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5e0-106">AzApiManagementGroup Cmdlet 會 **設定** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="fc5e0-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc5e0-107">EXAMPLES</span></span>

### <span data-ttu-id="fc5e0-108">範例1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="fc5e0-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="fc5e0-109">這個命令會設定一個名為 Group0001 的管理群組。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="fc5e0-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc5e0-110">PARAMETERS</span></span>

### <span data-ttu-id="fc5e0-111">-內容</span><span class="sxs-lookup"><span data-stu-id="fc5e0-111">-Context</span></span>
<span data-ttu-id="fc5e0-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fc5e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5e0-113">-DefaultProfile</span></span>
<span data-ttu-id="fc5e0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc5e0-115">-描述</span><span class="sxs-lookup"><span data-stu-id="fc5e0-115">-Description</span></span>
<span data-ttu-id="fc5e0-116">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="fc5e0-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fc5e0-117">-GroupId</span></span>
<span data-ttu-id="fc5e0-118">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="fc5e0-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc5e0-119">-Name</span></span>
<span data-ttu-id="fc5e0-120">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="fc5e0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc5e0-121">-PassThru</span></span>
<span data-ttu-id="fc5e0-122">passthru</span><span class="sxs-lookup"><span data-stu-id="fc5e0-122">passthru</span></span>

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

### <span data-ttu-id="fc5e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5e0-123">CommonParameters</span></span>
<span data-ttu-id="fc5e0-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5e0-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc5e0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5e0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fc5e0-126">INPUTS</span></span>

### <span data-ttu-id="fc5e0-127">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fc5e0-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc5e0-128">System.object</span><span class="sxs-lookup"><span data-stu-id="fc5e0-128">System.String</span></span>

### <span data-ttu-id="fc5e0-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fc5e0-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc5e0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="fc5e0-130">OUTPUTS</span></span>

### <span data-ttu-id="fc5e0-131">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fc5e0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="fc5e0-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fc5e0-132">NOTES</span></span>

## <span data-ttu-id="fc5e0-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc5e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="fc5e0-134">AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fc5e0-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="fc5e0-135">新-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fc5e0-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="fc5e0-136">移除-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fc5e0-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


