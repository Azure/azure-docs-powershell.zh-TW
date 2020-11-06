---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449512"
---
# <span data-ttu-id="61dda-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="61dda-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="61dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61dda-102">SYNOPSIS</span></span>
<span data-ttu-id="61dda-103">移除伺服器管理會話。</span><span class="sxs-lookup"><span data-stu-id="61dda-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="61dda-104">SYNTAX</span></span>

### <span data-ttu-id="61dda-105">ByName</span><span class="sxs-lookup"><span data-stu-id="61dda-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61dda-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="61dda-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61dda-107">說明</span><span class="sxs-lookup"><span data-stu-id="61dda-107">DESCRIPTION</span></span>
<span data-ttu-id="61dda-108">**AzureRmServerManagementSession** Cmdlet 會移除 Azure Server 管理會話。</span><span class="sxs-lookup"><span data-stu-id="61dda-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="61dda-109">示例</span><span class="sxs-lookup"><span data-stu-id="61dda-109">EXAMPLES</span></span>

## <span data-ttu-id="61dda-110">參數</span><span class="sxs-lookup"><span data-stu-id="61dda-110">PARAMETERS</span></span>

### <span data-ttu-id="61dda-111">-NodeName</span><span class="sxs-lookup"><span data-stu-id="61dda-111">-NodeName</span></span>
<span data-ttu-id="61dda-112">指定此 Cmdlet 移除會話之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="61dda-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61dda-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61dda-113">-ResourceGroupName</span></span>
<span data-ttu-id="61dda-114">指定會話所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61dda-114">Specifies the name of the resource group that the session belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61dda-115">-會話</span><span class="sxs-lookup"><span data-stu-id="61dda-115">-Session</span></span>
<span data-ttu-id="61dda-116">指定此 Cmdlet 移除的會話。</span><span class="sxs-lookup"><span data-stu-id="61dda-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="61dda-117">您可以使用這個參數，而不是 *ResourceGroupName* 、 *NodeName* 和 *SessionName* 參數。</span><span class="sxs-lookup"><span data-stu-id="61dda-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61dda-118">-SessionName</span><span class="sxs-lookup"><span data-stu-id="61dda-118">-SessionName</span></span>
<span data-ttu-id="61dda-119">指定此 Cmdlet 移除之會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="61dda-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dda-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dda-120">-DefaultProfile</span></span>
<span data-ttu-id="61dda-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61dda-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61dda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dda-122">CommonParameters</span></span>
<span data-ttu-id="61dda-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61dda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dda-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61dda-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dda-125">輸入</span><span class="sxs-lookup"><span data-stu-id="61dda-125">INPUTS</span></span>

### <span data-ttu-id="61dda-126">課時</span><span class="sxs-lookup"><span data-stu-id="61dda-126">Session</span></span>
<span data-ttu-id="61dda-127">參數 "Session" 接受管線中類型 "Session" 的值</span><span class="sxs-lookup"><span data-stu-id="61dda-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="61dda-128">輸出</span><span class="sxs-lookup"><span data-stu-id="61dda-128">OUTPUTS</span></span>

## <span data-ttu-id="61dda-129">筆記</span><span class="sxs-lookup"><span data-stu-id="61dda-129">NOTES</span></span>

## <span data-ttu-id="61dda-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="61dda-130">RELATED LINKS</span></span>

[<span data-ttu-id="61dda-131">AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="61dda-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="61dda-132">新-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="61dda-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


