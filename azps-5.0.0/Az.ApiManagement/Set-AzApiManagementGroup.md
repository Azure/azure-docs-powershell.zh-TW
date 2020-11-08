---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137594"
---
# <span data-ttu-id="9e970-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e970-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="9e970-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e970-102">SYNOPSIS</span></span>
<span data-ttu-id="9e970-103">配置 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="9e970-103">Configures an API management group.</span></span>

## <span data-ttu-id="9e970-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e970-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e970-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e970-105">DESCRIPTION</span></span>
<span data-ttu-id="9e970-106">AzApiManagementGroup Cmdlet 會 **設定** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="9e970-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="9e970-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e970-107">EXAMPLES</span></span>

### <span data-ttu-id="9e970-108">範例1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="9e970-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="9e970-109">這個命令會設定一個名為 Group0001 的管理群組。</span><span class="sxs-lookup"><span data-stu-id="9e970-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="9e970-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e970-110">PARAMETERS</span></span>

### <span data-ttu-id="9e970-111">-內容</span><span class="sxs-lookup"><span data-stu-id="9e970-111">-Context</span></span>
<span data-ttu-id="9e970-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="9e970-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9e970-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e970-113">-DefaultProfile</span></span>
<span data-ttu-id="9e970-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e970-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e970-115">-描述</span><span class="sxs-lookup"><span data-stu-id="9e970-115">-Description</span></span>
<span data-ttu-id="9e970-116">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="9e970-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="9e970-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9e970-117">-GroupId</span></span>
<span data-ttu-id="9e970-118">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e970-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="9e970-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e970-119">-Name</span></span>
<span data-ttu-id="9e970-120">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e970-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="9e970-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e970-121">-PassThru</span></span>
<span data-ttu-id="9e970-122">passthru</span><span class="sxs-lookup"><span data-stu-id="9e970-122">passthru</span></span>

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

### <span data-ttu-id="9e970-123">-確認</span><span class="sxs-lookup"><span data-stu-id="9e970-123">-Confirm</span></span>
<span data-ttu-id="9e970-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e970-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e970-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e970-125">-WhatIf</span></span>
<span data-ttu-id="9e970-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e970-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e970-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e970-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e970-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e970-128">CommonParameters</span></span>
<span data-ttu-id="9e970-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e970-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e970-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e970-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e970-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9e970-131">INPUTS</span></span>

### <span data-ttu-id="9e970-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9e970-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e970-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9e970-133">System.String</span></span>

### <span data-ttu-id="9e970-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9e970-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e970-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9e970-135">OUTPUTS</span></span>

### <span data-ttu-id="9e970-136">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9e970-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="9e970-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9e970-137">NOTES</span></span>

## <span data-ttu-id="9e970-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e970-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e970-139">AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e970-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="9e970-140">新-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e970-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="9e970-141">移除-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e970-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


